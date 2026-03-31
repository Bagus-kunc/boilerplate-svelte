# 🚀 SvelteCore | Premium Svelte 5 Boilerplate

Welcome to **SvelteCore**, the ultimate starting point for high-performance,
modern Svelte 5 applications. This boilerplate is meticulously crafted to
showcase the best of the latest web technologies, providing a premium developer
experience and a stunning visual foundation.

## 🌟 Key Features

- **⚡ Svelte 5 (Runes)**: Leverages the cutting-edge reactivity engine with
  `$state`, `$derived`, and `$effect` for ultra-efficient state management.

* **🎨 Tailwind CSS 4**: Utilizes the powerful, direct-to-CSS engine for rapid
  styling and modern design tokens.
* **🛡️ TypeScript Core**: Full type safety integrated throughout the entire
  project architecture.
* **✨ Premium Design System**:
  - **Typography**: Google Fonts Inter (UI) and Outfit (Display).
  - **Visuals**: Glassmorphic effects, smooth micro-animations, and a curated
    color palette.

- **🛠️ Professional Tooling**: Pre-configured with Vite, Vitest (Unit/Component
  testing), and Playwright (E2E testing).
- **📦 Lucide Icons**: A comprehensive set of high-quality, lightweight icons.

## 🏗️ Project Structure

```text
src/
├── lib/
│   ├── components/       # Premium UI components (Button, Navbar, Hero, etc.)
│   └── assets/           # Static assets and images
├── routes/
│   ├── +layout.svelte    # Root layout with theme initialization
│   ├── +page.svelte      # Modern Landing Page
│   └── layout.css        # Global CSS with Tailwind 4 @theme
└── app.html              # Main HTML template with font preloads
```

## 🚀 Quick Start

1. **Clone and Install Dependencies**:
   ```bash
   cd boilerplate-svelte
   npm install
   ```
2. **Start Development Server**:
   ```bash
   npm run dev
   ```
3. **Run Quality Checks**:
   ```bash
   npm run check    # Svelte & TypeScript check
   npm run lint     # Linting and formatting
   ```

## 🧪 Testing

- **Unit/Component Testing**:
  ```bash
  npm run test:unit
  ```
- **End-to-End Testing**:
  ```bash
  npm run test:e2e
  ```

## 🏗️ Building for Production

To create an optimized production bundle:

```bash
npm run build
```

You can preview the build locally using `npm run preview`.

## 📄 License

This project is open-source and free to use for any personal or professional
project.

---

Built with ❤️ for you.
