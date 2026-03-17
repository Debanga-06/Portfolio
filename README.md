<div align="center">

# 🌐 Debanga Guria — Personal Portfolio

**A modern, fully responsive developer portfolio built with pure HTML, CSS & JavaScript.**  
No frameworks. No dependencies. No build step. Just drop and deploy.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-debanga.vercel.app-e9c96e?style=for-the-badge&logo=vercel&logoColor=black)](https://debanga.vercel.app)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue?style=for-the-badge&logo=gnu&logoColor=white)](https://www.gnu.org/licenses/gpl-3.0)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

<br/>

![Portfolio Preview Dark](https://img.shields.io/badge/Theme-Dark%20%7C%20Light-e9c96e?style=flat-square)
![Responsive](https://img.shields.io/badge/Responsive-Mobile%20%7C%20Tablet%20%7C%20Desktop-4fd1c5?style=flat-square)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-4ade80?style=flat-square)

</div>

---

## ✨ Features

### Design & UX
- **Dark / Light Mode Toggle** — Smooth theme transition with `localStorage` persistence
- **Crystal Glassmorphism** — Layered floating cards with blur, translucency, and shimmer effects
- **Custom Cursor** — Gold dot with magnetic ring follow animation
- **Particle Network Background** — Dynamic connected particle system that adapts to theme
- **Typewriter Hero** — Cycles through roles with realistic typing & deletion animation
- **Scrolling Marquee** — Infinite skill ticker strip
- **Scroll Reveal Animations** — Staggered fade-up on every section as you scroll
- **Animated Skill Bars** — Progress bars that fill on scroll into view

### Sections
| Section | Description |
|---|---|
| 🦸 **Hero** | Name, animated role typewriter, stats, crystal card stack visual |
| 🚀 **Projects** | Real project cards with GitHub links, code snippets, ML pipeline diagrams |
| 👤 **About** | Bio, profile info card, availability status |
| 🛠️ **Skills** | Categorized skill cards + animated proficiency bars |
| 💼 **Experience** | Timeline of internships with "CURRENT" badge |
| 🎓 **Education** | Academic background cards |
| 🏆 **Certifications** | Verified credential cards |
| 📬 **Contact** | Email, LinkedIn, GitHub, Phone — all linked |

### Performance
- **Single HTML file** — Everything inlined, zero external JS dependencies
- **Google Fonts** — Only external resource (2 font families)
- **CSS Custom Properties** — Full theme system with instant variable switching
- **Intersection Observer API** — Efficient scroll-triggered animations
- **Vanilla JS only** — No React, no Vue, no build tools needed

---

## 🚀 Getting Started

### One-click deploy (Vercel — Recommended)

1. Fork or clone this repository
2. Go to [vercel.com](https://vercel.com) → **New Project**
3. Import your repository
4. Vercel auto-detects the static site — click **Deploy**
5. Your portfolio is live at `your-name.vercel.app` ✅

### Local development

```bash
# Clone the repository
git clone https://github.com/Debanga-06/portfolio.git
cd portfolio

# Open directly in browser — no build step needed
open index.html

# Or serve locally with any static server
npx serve .
# or
python -m http.server 8080
```

---

## 📁 Project Structure

```
portfolio/
│
├── portfoilo.html          # Complete portfolio — single self-contained file
├── README.md           # This file
└── LICENSE             # GNU General Public License v3.0
```

> Everything — HTML, CSS, and JavaScript — lives in `index.html`.  
> This is intentional: zero build complexity, instant deployment anywhere.

---

## 🎨 Customization Guide

### 1. Personal Information

Open `portfolio.html` and find these sections to update your details:

```html
<!-- Hero name -->
<h1 class="hname">
  <span class="ns">YourFirst</span>
  <span class="no">LastName</span>
</h1>

<!-- Hero description -->
<p class="hdesc">Your bio here...</p>

<!-- Stats -->
<div class="hsn">4<span>+</span></div>
<div class="hsl">Projects</div>
```

### 2. Typewriter Roles

Find the `roles` array in the `<script>` section:

```javascript
const roles = [
  'AI/ML Developer',
  'Python Engineer',
  'Cybersecurity Intern',
  'B.Tech CSE Student',
  'Problem Solver'
  // Add or change your roles here
];
```

### 3. Project Cards

Each project follows this pattern:

```html
<div class="pcard" style="--c1:#YOUR_COLOR_1;--c2:#YOUR_COLOR_2;">
  <div class="phdr">
    <div class="pico">🔐</div>   <!-- Change emoji -->
    <div class="pbags">
      <span class="pbag bag-s">Security</span>   <!-- Change badge -->
    </div>
  </div>
  <div class="pbody">
    <div class="pname">Project Name</div>
    <p class="pdesc">Project description...</p>
    <div class="pstack">
      <span class="ptag">Python</span>   <!-- Tech stack tags -->
    </div>
  </div>
  <div class="pfoot">
    <a href="https://github.com/YOUR_USERNAME/REPO" target="_blank" class="plink">
      View on GitHub
    </a>
  </div>
</div>
```

### 4. Color Theme

The entire color system uses CSS custom properties. Find `:root` and `[data-theme]` blocks:

```css
[data-theme="dark"] {
  --gold: #e9c96e;     /* Primary accent color */
  --teal: #4fd1c5;     /* Secondary accent */
  --rose: #fb7185;     /* Highlight / badges */
  --vio:  #a78bfa;     /* Violet accent */
  /* ... change any values to retheme instantly */
}
```

### 5. Skills & Proficiency Bars

Update the `data-pct` attribute to change bar fill percentages:

```html
<div class="proffill" data-pct="85"></div>  <!-- 85% fill -->
```

---

## 🖥️ Browser Support

| Browser | Support |
|---|---|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ✅ Full |

> Requires `backdrop-filter` support for glassmorphism effects. All modern browsers qualify.

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout |
|---|---|
| `> 1024px` | Two-column hero, two-column about, side-by-side project details |
| `768px – 1024px` | Single-column hero (visual card hidden), two-column grids retained |
| `< 768px` | Fully single-column, nav links hidden, mobile-optimized spacing |

---

## 🔗 Projects Featured

### 🔐 [CipherNest](https://github.com/Debanga-06/CipherNest)
A secure text-hiding tool combining **steganography and cryptography** to conceal sensitive data inside carrier files. Demonstrates applied security engineering and Python OOP design.

- **Tech:** Python, Cryptography, Steganography
- **Skills:** Applied cryptography · Cybersecurity · Secure data handling

### 🤖 [CirculoMetrix AI](https://github.com/Debanga-06/CirculoMetrix-AI)
An **AI-powered metrics and analytics platform** applying machine learning to analyze and derive insights from complex data patterns. End-to-end ML pipeline from ingestion to intelligent output.

- **Tech:** Python, Machine Learning, Data Analysis, AI/ML
- **Skills:** ML pipeline design · Data science · Pattern recognition

---

## 👤 About

**Debanga Guria**  
B.Tech Computer Science (AI-ML) Student  
Brainware University, Barasat, West Bengal

- 📧 [debanga078@gmail.com](mailto:debanga078@gmail.com)
- 💼 [linkedin.com/in/debanga-guria](https://www.linkedin.com/in/debanga-guria)
- 🐙 [github.com/Debanga-06](https://github.com/Debanga-06)
- 🌐 [debanga.vercel.app](https://debanga.vercel.app)

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0**.

```
Copyright (C) 2026  Debanga Guria

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <https://www.gnu.org/licenses/>.
```

See the [LICENSE](LICENSE) file for the full license text.

> **What GPL v3 means for this project:**
> - ✅ You may use, copy, and distribute this portfolio template
> - ✅ You may modify it and create derivative works
> - ✅ Commercial use is permitted
> - ⚠️ Any derivative work **must** also be released under GPL v3
> - ⚠️ Source code **must** be made available when distributing
> - ⚠️ Original copyright and license notices **must** be preserved

---

## 🙏 Acknowledgements

- **[Google Fonts](https://fonts.google.com)** — Bricolage Grotesque, Instrument Sans, JetBrains Mono
- **[Vercel](https://vercel.com)** — Hosting platform
- **[IBM Technovate Workshop](https://www.ibm.com)** — AI training and inspiration
- **[Edunet Foundation / AICTE](https://edunetfoundation.org)** — Cybersecurity internship program

---

<div align="center">

**Made with 💛 by [Debanga Guria](https://debanga.vercel.app)**

*B.Tech CSE (AI-ML) · Brainware University · West Bengal, India*

⭐ **Star this repo if it helped you!** ⭐

</div>