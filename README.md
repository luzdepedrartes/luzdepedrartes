<div align="center">

# ✨ LUZ DE PEDRA ✨

### *Pintura Marmorizada de Luxo*

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=for-the-badge&logo=react&logoColor=white&labelColor=black)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0.8-646CFF?style=for-the-badge&logo=vite&logoColor=white&labelColor=black)](https://vitejs.dev/)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Deployed-222222?style=for-the-badge&logo=githubpages&logoColor=white&labelColor=black)](https://centronictec.github.io/luzdepedra/)

![Luz de Pedra Banner](https://via.placeholder.com/1200x400/0A0A0A/FFD700?text=Luz+de+Pedra)

</div>

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Arquitetura do Software](#-arquitetura-do-software)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Boas Práticas Implementadas](#-boas-práticas-implementadas)
- [Design System](#-design-system)
- [Performance e SEO](#-performance-e-seo)
- [Como Executar](#-como-executar)
- [Deploy no GitHub Pages](#-deploy-no-github-pages)
- [Customização](#-customização)
- [Créditos](#-créditos)

---

## 🎯 Sobre o Projeto

**Luz de Pedra** é uma aplicação web institucional desenvolvida para apresentar serviços de pintura marmorizada de luxo. O projeto combina uma experiência visual premium com performance otimizada, oferecendo uma galeria interativa de obras e canal de contato direto.

### ✨ Diferenciais

- 🎨 **Design Premium**: Tema preto e ouro com animações dinâmicas
- 📱 **100% Responsivo**: Adaptação perfeita para todos os dispositivos
- ⚡ **Performance Otimizada**: Lazy loading, code splitting e otimização de assets
- 🖼️ **Galeria Interativa**: Modal com informações detalhadas de cada obra
- 📞 **Contato Integrado**: WhatsApp, Instagram e formulário funcional

---

## 🏗️ Arquitetura do Software

### **Arquitetura Hexagonal (Ports & Adapters)**

```mermaid
graph TB
    subgraph "Camada de Apresentação"
        A[React Components]
        B[Pages]
        C[CSS Modules]
    end
    
    subgraph "Camada de Lógica de Negócio"
        D[Custom Hooks]
        E[Context API]
        F[Data Services]
    end
    
    subgraph "Camada de Dados"
        G[Local Storage]
        H[FormSubmit API]
        I[External Links]
    end
    
    A --> D
    B --> E
    C --> F
    D --> G
    E --> H
    F --> I
Padrões de Design Utilizados
Padrão	Aplicação	Benefício
Component Pattern	Componentes reutilizáveis (GalleryItem, OptimizedImage)	Manutenibilidade e reuso
Container Pattern	Separação de lógica e apresentação	Testabilidade e organização
Lazy Loading	Carregamento sob demanda de componentes	Performance inicial otimizada
Custom Hooks	useIntersectionObserver, useLocalStorage	Reuso de lógica stateful
CSS Modules	Estilização isolada por componente	Evita conflitos globais
📁 Estrutura do Projeto
text
luzdepedra/
│
├── public/
│   ├── .nojekyll          # Necessário para GitHub Pages
│   └── vite.svg           # Favicon
│
├── src/
│   ├── assets/
│   │   ├── imagens/       # Imagens originais (img1.png a img9.png)
│   │   └── thumbnails/    # Miniaturas geradas automaticamente
│   │
│   ├── components/
│   │   ├── common/
│   │   │   ├── OptimizedImage.jsx    # Componente de imagem otimizada
│   │   │   └── Modal.jsx             # Modal reutilizável
│   │   ├── Gallery.jsx               # Galeria principal
│   │   ├── GalleryItem.jsx           # Item da galeria
│   │   ├── Contact.jsx               # Formulário de contato
│   │   ├── Gallery.css               # Estilos da galeria
│   │   └── Contact.css               # Estilos do contato
│   │
│   ├── data/
│   │   └── galleryData.js   # Dados centralizados das imagens
│   │
│   ├── App.jsx              # Componente raiz
│   ├── main.jsx             # Ponto de entrada
│   └── index.css            # Estilos globais (design system)
│
├── scripts/
│   └── optimize-images.js   # Script de otimização de imagens
│
├── index.html               # Template HTML
├── vite.config.js          # Configuração do Vite
├── package.json            # Dependências e scripts
└── README.md               # Documentação
🛠️ Tecnologias Utilizadas
Frontend Core
Tecnologia	Versão	Propósito
React	18.2.0	Biblioteca UI
Vite	5.0.8	Build tool e dev server
React DOM	18.2.0	Renderização React
Estilização e UI
Tecnologia	Propósito
CSS3 Variables	Design system dinâmico
CSS Modules	Estilização isolada
Google Fonts	Tipografia premium (Cormorant, Montserrat)
Ícones e Assets
Biblioteca	Propósito
React Icons	Ícones oficiais (WhatsApp, Instagram)
DevOps e Deploy
Ferramenta	Propósito
gh-pages	Deploy no GitHub Pages
Terser	Minificação de código
✅ Boas Práticas Implementadas
1. Performance
javascript
// ✅ Lazy loading de imagens
<OptimizedImage src={src} lazy={true} />

// ✅ Code splitting automático
manualChunks: { vendor: ['react', 'react-dom'] }

// ✅ Pré-carregamento de recursos
<link rel="preconnect" href="https://fonts.googleapis.com" />
2. SEO e Acessibilidade
html
<!-- ✅ Meta tags otimizadas -->
<meta name="description" content="Luz de Pedra - Pintura Marmorizada de Luxo" />
<meta name="theme-color" content="#000000" />

<!-- ✅ Estrutura semântica -->
<header>, <main>, <section>, <footer>, <nav>
3. Responsividade
css
/* ✅ Design mobile-first com clamp() */
font-size: clamp(0.8rem, 3vw, 1.2rem);

/* ✅ Breakpoints estratégicos */
@media (max-width: 768px) { }
@media (max-width: 480px) { }
4. Manutenibilidade
✅ Componentização: Componentes pequenos e reutilizáveis

✅ Centralização de dados: galleryData.js único ponto de verdade

✅ Variáveis CSS: Design system centralizado

✅ Documentação: README completo e comentários no código

🎨 Design System
Paleta de Cores
Cor	Código	Uso
Ouro Brilhante	#FFD700	Destaques primários
Ouro Claro	#FFF8DC	Hovers e gradientes
Ouro Escuro	#DAA520	Bordas e acentos
Preto Fundo	#0A0A0A	Background principal
Preto Card	#111111	Cards e containers
Cinza Texto	#C0C0C0	Textos secundários
Tipografia
Família	Uso	Pesos
Cormorant Garamond	Títulos e destaques	300-700
Montserrat	Corpo e navegação	300-700
Animações
css
/* ✅ Efeito de brilho pulsante */
@keyframes goldPulse {
  0%, 100% { text-shadow: 0 0 5px rgba(255, 215, 0, 0.3); }
  50% { text-shadow: 0 0 20px rgba(255, 215, 0, 0.6); }
}

/* ✅ Efeito de brilho ao hover */
.gallery-item:hover {
  box-shadow: 0 0 30px rgba(255, 215, 0, 0.4);
}
⚡ Performance e SEO
Lighthouse Score Alvo
Métrica	Desktop	Mobile
Performance	95+	90+
Acessibilidade	100	100
SEO	100	100
Melhores Práticas	95+	95+
Otimizações Implementadas
✅ Critical CSS inlined para renderização inicial

✅ Lazy loading em todas imagens

✅ Code splitting automático (vendor chunk)

✅ Preconnect para Google Fonts

✅ Compressão de imagens no build

✅ Minificação de CSS/JS

🚀 Como Executar
Pré-requisitos
bash
Node.js >= 18.0.0
npm >= 9.0.0
Instalação
bash
# 1. Clone o repositório
git clone https://github.com/centronictec/luzdepedra.git

# 2. Entre na pasta
cd luzdepedra

# 3. Instale as dependências
npm install --legacy-peer-deps

# 4. Execute em desenvolvimento
npm run dev

# 5. Acesse no navegador
http://localhost:5173/luzdepedra/
Comandos Disponíveis
Comando	Descrição
npm run dev	Inicia servidor de desenvolvimento
npm run build	Gera build de produção
npm run preview	Visualiza build localmente
npm run deploy	Publica no GitHub Pages
npm run optimize:images	Otimiza imagens (requer sharp)
🌐 Deploy no GitHub Pages
Configuração Automática
bash
# 1. Instale o gh-pages
npm install gh-pages --save-dev

# 2. Configure no package.json
{
  "homepage": "https://centronictec.github.io/luzdepedra"
}

# 3. Configure o vite.config.js
base: '/luzdepedra/'

# 4. Faça o deploy
npm run deploy
Estrutura de Build
text
dist/
├── assets/
│   ├── index-[hash].js
│   ├── index-[hash].css
│   └── img*.png
└── index.html
🎨 Customização
Cores e Temas
Edite as variáveis CSS em src/index.css:

css
:root {
  --gold-bright: #FFD700;    /* Altere para sua cor */
  --black-bg: #0A0A0A;       /* Cor de fundo */
}
Dados da Galeria
Edite src/data/galleryData.js:

javascript
const imageDescriptions = [
  {
    title: "Sua Obra",
    subtitle: "Subtítulo",
    description: "Descrição detalhada",
    date: "2024",
    style: "Estilo",
    location: "Local"
  }
]
Informações de Contato
Edite src/components/Contact.jsx:

javascript
const openWhatsApp = () => {
  window.open('https://wa.me/SEU-NUMERO', '_blank')
}
📞 Créditos
<div align="center">
Desenvolvido por Centronic Tecnologia LTDA

🚀 Tecnologia e inovação para transformar ideias em realidade

https://img.shields.io/badge/GitHub-centronictec-222222?style=flat-square&logo=github
https://img.shields.io/badge/Email-depedraluz@gmail.com-FFD700?style=flat-square&logo=gmail

</div>
📄 Licença
Este projeto é 100% Open Source e está sob a licença MIT.

<div align="center">
✨ Valorize seu ambiente e traga requinte com a pintura marmorizada ✨
Site: https://centronictec.github.io/luzdepedra/

</div> ```
