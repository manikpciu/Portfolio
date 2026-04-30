# 🚀 Manik Mia — Portfolio Website

A professional, fast, and fully customizable portfolio built with **plain HTML, CSS & JavaScript** powered by **Vite** for development speed.

---

## 📁 Project Structure

```
portfolio/
├── index.html           ← Main page (add sections here)
├── src/
│   ├── style.css        ← All styling (edit colors, fonts here)
│   ├── main.js          ← All JavaScript interactions
│   └── assets/          ← Put your images/icons here
├── public/              ← Static files (favicon, CV PDF, etc.)
├── package.json
└── vite.config.js
```

---

## ⚡ Getting Started (VS Code)

### Step 1 — Install Node.js
Download from: https://nodejs.org (choose LTS version)

### Step 2 — Open in VS Code
```bash
# Open terminal in VS Code (Ctrl + `)
cd portfolio
```

### Step 3 — Install Dependencies
```bash
npm install
```

### Step 4 — Start Dev Server
```bash
npm run dev
```
Browser-এ `http://localhost:5173` খুলবে। File save করলেই auto-refresh হবে।

### Step 5 — Build for Production
```bash
npm run build
```
`dist/` folder তৈরি হবে — এটাই deploy করতে হবে।

---

## ✏️ How to Customize (কীভাবে আপডেট করবে)

### 🎨 Change Colors / Theme
`src/style.css` এর উপরে `:root` section:
```css
:root {
  --bg:      #0a0a0f;    /* Background color */
  --accent:  #6c63ff;    /* Main accent color */
  --accent2: #ff6584;    /* Secondary accent */
  --text:    #e8e8f0;    /* Text color */
}
```
এখানে color change করলেই পুরো site এর theme বদলে যাবে।

### 👤 Add Your Photo
1. তোমার photo `src/assets/photo.jpg` এ রাখো
2. `index.html` এ এই অংশ খোঁজো:
```html
<div class="avatar-placeholder">MM</div>
```
Replace করো:
```html
<img src="/src/assets/photo.jpg" alt="Manik Mia" />
```

### 📌 Update Personal Info
`index.html` এ সরাসরি edit করো:
- নাম, Bio, Location
- Email, GitHub, LinkedIn links
- Stats (Projects count, Years, Clients)

### ➕ Add a New Project
`index.html` এ projects section এ নতুন card paste করো:
```html
<div class="project-card reveal">
  <div class="project-img">
    <!-- Option 1: Emoji placeholder -->
    <div class="project-img-placeholder">🔥</div>
    <!-- Option 2: Real screenshot -->
    <!-- <img src="/src/assets/project4.png" alt="Project Name" /> -->
  </div>
  <div class="project-info">
    <div class="project-tags">
      <span>React</span><span>Firebase</span>
    </div>
    <h3>Your Project Name</h3>
    <p>Short description of what this project does.</p>
    <div class="project-links">
      <a href="https://yourproject.com" target="_blank" class="btn btn-sm">Live Demo ↗</a>
      <a href="https://github.com/you/repo" target="_blank" class="btn btn-sm btn-outline">GitHub ↗</a>
    </div>
  </div>
</div>
```

### 🛠️ Add a New Skill
`index.html` এর skills section এ:
```html
<span class="tag">New Skill</span>
```

### 📧 Connect Contact Form (Real Emails)
`src/main.js` এ form submit section এ [Formspree](https://formspree.io) যোগ করো:
```js
const response = await fetch('https://formspree.io/f/YOUR_ID', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name, email, message })
});
```

### 📄 Add CV / Resume
1. `public/cv.pdf` এ তোমার CV রাখো
2. `index.html` এ এই link update করো:
```html
<a href="/cv.pdf" class="btn btn-primary" download>Download CV ↓</a>
```

---

## 🌐 Deploy করার Options

### Option 1 — Vercel (Recommended, Free)
```bash
npm install -g vercel
vercel
```
অথবা GitHub এ push করে vercel.com থেকে import করো।

### Option 2 — Netlify (Free)
```bash
npm run build
# dist/ folder টা netlify.com এ drag-and-drop করো
```

### Option 3 — GitHub Pages (Free)
```bash
npm install -D gh-pages
# package.json scripts এ add করো:
# "deploy": "gh-pages -d dist"
npm run build && npm run deploy
```

---

## 🆕 Add New Sections

নতুন section add করতে `index.html` এ template:
```html
<section class="section" id="new-section">
  <div class="container">
    <div class="section-label reveal">Label</div>
    <h2 class="section-title reveal">Title <span class="highlight">here</span></h2>
    <!-- content -->
  </div>
</section>
```
Navbar এও link যোগ করো:
```html
<li><a href="#new-section">New Section</a></li>
```

---

## 📦 Dependencies

| Package | Purpose |
|---------|---------|
| vite    | Fast dev server + build tool |

শুধু একটাই dependency — super lightweight!

---

Built with ❤️ by Manik Mia
