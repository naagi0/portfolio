# 🧑‍💻 Tanmay Shukla — Developer Portfolio

> A terminal-aesthetic, dark-themed personal portfolio website built with pure HTML, CSS, and Vanilla JavaScript. No frameworks, no build tools, no dependencies — just open and run.

---

## 📸 Preview

```
┌─────────────────────────────────────────────┐
│  ~/tanmay-shukla          [about] [skills]  │
│─────────────────────────────────────────────│
│                                             │
│  Hi, I'm                ┌──────────────┐   │
│  Tanmay Shukla.         │ tanmay@dev:~ │   │
│                         │ ❯ cat profile│   │
│  $ Web Developer_       │ { "name":... │   │
│                         └──────────────┘   │
│  [ ↗ View Projects ]  [ ⬇ Resume ]         │
└─────────────────────────────────────────────┘
```

---

## 🗂️ Project Structure

```
portfolio/
│
├── portfolio.html        # Single-file portfolio (HTML + CSS + JS)
└── README.md             # This file
```

> The entire portfolio lives in **one self-contained HTML file**. No build step, no package manager, no server required.

---

## 🚀 How to Run

### ✅ Option 1 — Just Open in Browser (Easiest)

1. Download `portfolio.html`
2. Double-click the file
3. It opens directly in your browser — done ✅

---

### 🌐 Option 2 — Serve Locally (Recommended for Development)

If you want live-reload while editing, use any local server:

**Using Python (built-in, no install needed):**
```bash
# Python 3
python -m http.server 3000

# Then open → http://localhost:3000/portfolio.html
```

**Using Node.js (`npx serve`):**
```bash
npx serve .
# Then open → http://localhost:3000
```

**Using VS Code:**
- Install the **Live Server** extension
- Right-click `portfolio.html` → `Open with Live Server`

---

### ☁️ Option 3 — Deploy to Vercel (Free Hosting)

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Run from the project folder
vercel

# Follow the prompts — your site will be live at:
# https://your-project.vercel.app
```

**Or deploy via Vercel Dashboard (no CLI):**
1. Go to [vercel.com](https://vercel.com)
2. Click **New Project** → Import from GitHub
3. Select your repo → Click **Deploy**

---

### 📄 Option 4 — GitHub Pages (Free Hosting)

1. Push `portfolio.html` to a GitHub repo
2. Rename it to `index.html`
3. Go to repo **Settings → Pages**
4. Set source to `main` branch → `/ (root)`
5. Your site will be live at `https://<username>.github.io/<repo>/`

---

## 🛠️ Languages & Tools Used

### 🔤 Languages

| Language | Usage |
|----------|-------|
| **HTML5** | Page structure, semantic markup, all sections |
| **CSS3** | Styling, animations, responsive layout, CSS variables |
| **JavaScript (ES6+)** | Typing animation, scroll effects, hamburger menu, form handling, contribution graph |

---

### 🎨 Styling & Design

| Tool / Technique | Purpose |
|-----------------|---------|
| **CSS Custom Properties** | Theme tokens — colors, fonts, spacing |
| **CSS Grid** | Hero, about, skills, projects, contact layouts |
| **CSS Flexbox** | Nav, buttons, cards, tag rows |
| **CSS Animations** | Cursor blink, pulse dot, fade-in on scroll |
| **`@keyframes`** | `blink`, `pulse` animations |
| **Backdrop Filter** | Frosted glass navbar |
| **Repeating Gradients** | Scan-line overlay, grid background, card textures |
| **`clamp()`** | Fluid typography and spacing (mobile → desktop) |
| **Media Queries** | Mobile-first responsive breakpoints (`max-width: 768px`) |

---

### 🔡 Fonts

| Font | Source | Usage |
|------|--------|-------|
| **JetBrains Mono** | Google Fonts | Body text, code, terminal elements |
| **Syne** | Google Fonts | Headings, name, section titles |

> Loaded via `<link>` from `fonts.googleapis.com` — no local files needed.

---

### ⚙️ JavaScript Features

| Feature | How it works |
|---------|-------------|
| **Typing animation** | Custom `typeLoop()` — cycles through role strings, types & deletes with configurable speed |
| **Contribution graph** | Procedurally generated 52×7 grid with random activity levels (`l1`–`l4`) |
| **Scroll fade-in** | `IntersectionObserver` API watches `.fade-in` elements and adds `.visible` class |
| **Hamburger menu** | Toggle `open` class on nav and mobile menu elements |
| **Contact form** | `onsubmit` intercept → shows toast notification → resets form |
| **Resume button** | Click handler (replace `alert` with actual PDF link before going live) |

---

### 🌍 External Dependencies

| Dependency | Type | CDN / Source |
|------------|------|--------------|
| **Google Fonts** | Font CDN | `fonts.googleapis.com` |

> That's it. No npm packages, no React, no Webpack, no Tailwind CLI — 100% dependency-free at runtime.

---

## ✏️ How to Customise

Open `portfolio.html` in any text editor and update these sections:

### 1. Personal Info
```html
<!-- Line ~170 — Hero name -->
<h1 class="hero-name">Hi, I'm<br/>Tanmay Shukla.</h1>

<!-- Terminal card — update JSON values -->
<span class="term-str">"Tanmay Shukla"</span>
<span class="term-str">"Kanpur, UP, India"</span>
```

### 2. Typing Roles
```js
// In the <script> block at the bottom
const roles = ["Web Developer", "React.js Developer", "Django Developer", ...];
```

### 3. Social Links
```html
<a href="https://github.com/naagi0" ...>  <!-- GitHub -->
<a href="mailto:tanmayshukla0408@gmail.com" ...>  <!-- Email -->
```

### 4. Resume PDF
```js
// Replace the alert() with your actual PDF URL
document.getElementById('resume-btn').addEventListener('click', e => {
  e.preventDefault();
  window.open('https://your-resume-link.pdf', '_blank');
});
```

### 5. Project Live Demo Links
```html
<!-- Find each project card and update href="#" -->
<a href="https://your-live-demo.vercel.app" class="project-link">↗ Live Demo</a>
```

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout |
|-----------|--------|
| **> 768px** | 2-column grid (hero, about, contact), horizontal nav |
| **≤ 768px** | Single column, hamburger menu, compressed contribution graph |

---

## 🎨 Color Palette

| Token | Hex | Used for |
|-------|-----|---------|
| `--bg` | `#080c10` | Page background |
| `--bg2` | `#0d1117` | Cards, inputs |
| `--bg3` | `#111820` | Terminal bar, skill icons |
| `--green` | `#00ff88` | Accent, CTA, active states |
| `--cyan` | `#38bdf8` | Secondary accent, tags |
| `--purple` | `#a78bfa` | Timeline techs, blog tags |
| `--orange` | `#fb923c` | Terminal strings |
| `--text` | `#c9d8e8` | Body text |
| `--muted` | `#4d6478` | Subtitles, placeholders |
| `--white` | `#e8f4ff` | Headings |
| `--line` | `#1c2a3a` | Borders, dividers |

---

## 📋 Sections Overview

| # | Section | Description |
|---|---------|-------------|
| 01 | **Hero** | Name, typing animation, terminal card, CTA buttons, social links |
| 02 | **About** | Bio, stats (5 projects, 4 certs, graduating 2026), tech stack pills |
| 03 | **Skills** | 6 categories — Languages, Frontend, Backend, Data/ML, Databases, DevOps |
| 04 | **Projects** | 5 project cards with description, tags, GitHub & demo links |
| 05 | **Certifications** | GitHub activity graph + 4 certifications + SIH achievement |
| 06 | **Education** | Vertical timeline — B.Tech MPEC → ISC → ICSE |
| 07 | **Contact** | Email, phone, open-to status, working contact form |

---

## 🧪 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| IE 11 | ❌ Not supported |

> Uses `IntersectionObserver`, `CSS Grid`, `clamp()`, `backdrop-filter`, and `CSS Custom Properties` — all supported in modern browsers.

---

## 📬 Contact

**Tanmay Shukla**
- 📧 [tanmayshukla0408@gmail.com](mailto:tanmayshukla0408@gmail.com)
- 🐙 [github.com/naagi0](https://github.com/naagi0)
- 📍 Kanpur, UP, India

---

<p align="center">Built with ❤️ and too much ☕ · 2026</p>
