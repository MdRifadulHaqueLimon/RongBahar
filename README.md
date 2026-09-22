<div align="center">

<img src="https://img.icons8.com/?size=100&id=XrEFnp33pJYw&format=png&color=000000" width="80" alt="RongBahar Logo">

# 🛍️ RongBahar

### A Modern, Fully Responsive E-Commerce Frontend

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Responsive](https://img.shields.io/badge/Responsive-Yes-success)](https://)
[![Bilingual](https://img.shields.io/badge/Languages-EN%20%7C%20BN-orange)]()

**Live Demo:** [rongbahar-demo.vercel.app](https://) *(Deploy & add your link)*

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Screenshots](#-screenshots)
- [Architecture](#-architecture)
- [Challenges & Solutions](#-challenges--solutions)
- [File Structure](#-file-structure)
- [Getting Started](#-getting-started)
- [Responsive Breakpoints](#-responsive-breakpoints)
- [Future Roadmap](#-future-roadmap)
- [Developer](#-developer)
- [License](#-license)

---

## 🎯 Overview

**RongBahar** is a production-grade e-commerce frontend application built entirely with **vanilla web technologies** — no frameworks, no libraries, no backend. It demonstrates how far pure HTML, CSS, and JavaScript can go when architected with care.

> Designed as a **portfolio showcase** and **frontend skills demonstration**, RongBahar simulates a complete online shopping experience including product browsing, cart management, user authentication, bilingual support, and order checkout — all running entirely in the browser.

### Why Frontend-Only?
- ✅ **Zero server cost** — runs from `file://` or any static host
- ✅ **No database setup** — in-memory state management
- ✅ **Instant deployment** — works on GitHub Pages, Netlify, Vercel
- ✅ **Form submission** via FormSubmit.co (no backend needed)

---

## ✨ Key Features

| Feature | Description | Status |
|---------|-------------|--------|
| 🎠 **Auto Hero Slider** | 4-slide carousel with auto-play, dot indicators, prev/next arrows, pause on hover/touch | ✅ |
| 🔍 **Live Search & Filter** | Real-time product search + category tab filtering | ✅ |
| 🛒 **Shopping Cart** | Add, quantity adjust, remove items with real-time total calculation | ✅ |
| 🔐 **User Authentication** | Sign In, Sign Up, Google Sign-In (demo) with form validation | ✅ |
| 🌐 **Bilingual Support** | Full English ↔ Bengali switch including product names & FAQ | ✅ |
| 📱 **Mobile Nav Drawer** | Animated hamburger menu with glassmorphism slide-in panel | ✅ |
| 📦 **Email Checkout** | Order form submits directly to owner email via FormSubmit.co | ✅ |
| ❓ **FAQ Accordion** | Smooth expand/collapse with auto-close behavior | ✅ |
| 🎨 **Glassmorphism UI** | Frosted glass cards, gradient borders, ambient floating blobs | ✅ |
| 📐 **Fully Responsive** | Optimized for 280px (watch) to 1400px+ (desktop) | ✅ |

---

## 🛠 Tech Stack

### Core
- **HTML5** — Semantic structure, accessibility, SEO
- **CSS3** — Grid, Flexbox, Custom Properties, Animations, Glassmorphism
- **JavaScript ES6+** — DOM manipulation, state management, Fetch API

### Design
- **Google Fonts** — Baloo 2, Hind Siliguri, Inter
- **SVG Icons** — Inline scalable vectors
- **Unsplash** — Hero & about section imagery
- **Picsum** — Product placeholder images

### Services
- **FormSubmit.co** — Backend-less form handling via AJAX

---

## 📸 Screenshots

<div align="center">

| Desktop View | Mobile View |
|:---:|:---:|
| *Add desktop screenshot* | *Add mobile screenshot* |

| Hero Slider | Product Grid | Cart Drawer |
|:---:|:---:|:---:|
| *Add slider screenshot* | *Add grid screenshot* | *Add cart screenshot* |

</div>

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────┐
│              index.html                      │
│   (Semantic Structure + Content)             │
└────────────────────┬────────────────────────┘
                     │
        ┌────────────┴────────────┐
        ▼                         ▼
┌──────────────┐        ┌──────────────┐
│   style.css  │        │  script.js   │
│   (Design)   │        │   (Logic)    │
└──────┬───────┘        └──────┬───────┘
       │                       │
       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐
│ CSS Variables   │    │ In-Memory State │
│ Grid + Flexbox  │    │ Event Listeners │
│ Animations      │    │ DOM Rendering   │
│ Media Queries   │    │ Fetch API       │
└─────────────────┘    └─────────────────┘
```

### State Management (In-Memory)
```javascript
let cart = [];          // [{id, qty}]
let users = [];         // [{name, phone, email, password}]
let currentUser = null; // Active session user
let activeCat = 'all';  // Current category filter
let currentLang = 'en'; // Active language
```

---

## 🧩 Challenges & Solutions

| # | Challenge | Solution |
|---|-----------|----------|
| 1 | **Glassmorphism cross-browser** | `backdrop-filter` + `-webkit-` fallback + solid rgba base layer |
| 2 | **No persistent storage** | Pure in-memory state with reactive UI re-renders on every mutation |
| 3 | **Bilingual dynamic content** | Central `TRANSLATIONS` object with `data-i18n` attribute binding |
| 4 | **Slider on all screen sizes** | `clamp()` fluid typography + `aspect-ratio` adaptive heights |
| 5 | **Forms without backend** | FormSubmit.co AJAX POST with JSON payload to email |
| 6 | **Smooth FAQ accordion** | `max-height: 0 → 300px` CSS transition with overflow hidden |
| 7 | **Multiple modal stacking** | Strict z-index hierarchy (55→100) + unified `closeAll()` handler |

---

## 📁 File Structure

```
RongBahar/
│
├── index.html          # Page structure, modals, drawers
├── style.css           # All styles: layout, animations, responsive
├── script.js           # All logic: state, render, events, API
│
├── RongBahar_Documentation.md      # Full technical documentation
├── RongBahar_Summary.md            # Executive summary
├── RongBahar_Presentation.md       # Slide deck (12 slides)
└── RongBahar_GitHub_Setup.md       # Repo setup guide
```

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No build tools, no dependencies, no installation

### Run Locally
```bash
# Clone the repository
git clone https://github.com/MdRifadulHaqueLimon/RongBahar.git

# Navigate to project
cd RongBahar

# Open in browser (macOS)
open index.html

# Open in browser (Linux)
xdg-open index.html

# Or simply double-click index.html
```

### Deploy
Works on any static hosting platform:
- [GitHub Pages](https://pages.github.com/)
- [Netlify](https://netlify.com/)
- [Vercel](https://vercel.com/)
- [Surge](https://surge.sh/)

---

## 📐 Responsive Breakpoints

| Breakpoint | Target | Grid | Key Adjustments |
|------------|--------|------|-----------------|
| `≤280px` | Smartwatch | 1 col | Minimal UI, hidden text |
| `≤360px` | Small phone | 2 col | Compact slider, small fonts |
| `≤480px` | Standard phone | 2 col | 16:9 about image |
| `≤640px` | Large phone | 2 col | Full mobile layout |
| `≤768px` | Tablet portrait | 2 col | Stacked about, 2-col footer |
| `≤1024px` | Tablet landscape | Auto | Side-by-side layouts |
| `≥1400px` | Desktop | Auto-fill | Large grids, max spacing |

---

## 🔮 Future Roadmap

```
Phase 1 — Backend Integration
├── Firebase / MongoDB database
├── JWT-based authentication
├── Persistent cart & sessions
└── Order history storage

Phase 2 — Payments & Admin
├── bKash / Nagad / Stripe integration
├── Admin dashboard (product CRUD)
├── Order management system
└── Inventory tracking

Phase 3 — Advanced Features
├── PWA with offline support
├── Real-time chat (WebSocket)
├── Push notifications
├── Analytics & reporting
└── AI product recommendations
```

---

## 👨‍💻 Developer

**Md. Rifadul Haque Limon**

> Frontend Developer & Shopify Designer

- 🌐 **Portfolio**: [MdRifadulHaqueLimon](https://mdrifadulhaquelimon.github.io/MdRifadulHaqueLimon/)
- 📧 **Email**: [mrrifadulhaquelimon@gmail.com](mailto:mrrifadulhaquelimon@gmail.com)
- 📱 **Phone**: +880 1644-881780
- 💼 **LinkedIn**: [linkedin.com/in/mdrifadulhaquelimon](https://www.linkedin.com/in/mdrifadulhaquelimon/)
- 🐙 **GitHub**: [github.com/MdRifadulHaqueLimon](https://github.com/MdRifadulHaqueLimon)
- 📘 **Facebook**: [facebook.com/likonkhan76](https://www.facebook.com/likonkhan76)

---

## 📄 License

This project is built for **portfolio and demonstration purposes**.

```
© 2026 RongBahar. All rights reserved.
```

---

<div align="center">

⭐ **Star this repo if you found it useful!**

**[⬆ Back to Top](#-rongbahar)**

</div>
