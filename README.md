# 🚀 Tailwind CSS v4 + DaisyUI Boilerplate

This is a ready-to-use boilerplate for building landing pages with **Tailwind CSS v4** and **DaisyUI**.

---

## 📂 Project Structure

```
landingpage/
 ├── public/
 │    └── index.html
 ├── src/
 │    └── input.css
 ├── dist/
 │    └── output.css  (auto-generated)
 ├── package.json
```

---

## 🛠 Setup Instructions

### 1. Initialize Project
```bash
yarn init -y
yarn add -D tailwindcss daisyui
```

### 2. Input CSS (`src/input.css`)
```css
@import "tailwindcss/preflight"; /* resets & base styles */
@import "tailwindcss/utilities"; /* utility classes */
@plugin "daisyui";               /* enable DaisyUI */
@source "./public/*.{html,js}";  /* watch HTML & JS */
```

### 3. Example HTML (`public/index.html`)
```html
<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DaisyUI v4 Landing Page</title>
  <link rel="stylesheet" href="../dist/output.css">
</head>
<body>

  <!-- Navbar -->
  <div class="navbar bg-base-100 shadow">
    <div class="flex-1">
      <a class="btn btn-ghost text-xl">Brand</a>
    </div>
    <div class="flex-none">
      <ul class="menu menu-horizontal px-1">
        <li><a>Home</a></li>
        <li><a>About</a></li>
        <li><a>Contact</a></li>
      </ul>
    </div>
  </div>

  <!-- Hero -->
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-md">
        <h1 class="text-5xl font-bold">Hello, Tailwind v4</h1>
        <p class="py-6">Now using @import instead of @tailwind, with DaisyUI for prebuilt components.</p>
        <button class="btn btn-primary">Get Started</button>
      </div>
    </div>
  </div>

</body>
</html>
```

---

## 🚀 Build & Watch

Add this script to your `package.json`:

```json
"scripts": {
  "dev": "tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
}
```

Run it:
```bash
yarn dev
```

---

## ✅ Features
- Tailwind CSS v4
- DaisyUI prebuilt components
- Responsive navbar + hero section
- Minimal, interview-ready setup

---

## 📖 Notes
- In Tailwind v4, `@tailwind base;` is replaced with `@import "tailwindcss/preflight"`.
- Use `@plugin` and `@source` directly inside CSS (no need for `tailwind.config.js` unless customization is needed).
