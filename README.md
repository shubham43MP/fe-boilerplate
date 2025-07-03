# ⚡ React + TypeScript + Vite Boilerplate

A fully-configured modern frontend boilerplate using React, TypeScript, Vite, pnpm, Prettier, Husky, and recommended best practices. Focused on performance, consistency, and team collaboration.

---

## 📦 Tech Stack

- ⚡ [Vite](https://vitejs.dev/)
- ⚛️ [React](https://reactjs.org/)
- ✨ [TypeScript](https://www.typescriptlang.org/)
- 📦 [pnpm](https://pnpm.io/)
- 🎨 [Prettier](https://prettier.io/)
- 🐶 [Husky](https://typicode.github.io/husky/)
- 🔒 [lint-staged](https://github.com/okonet/lint-staged)

---

## 🛠️ Project Setup

### ✅ 1. Install pnpm globally

```bash
npm install -g pnpm
```

---

### ✅ 2. Create the app

```bash
pnpm create vite
# → Choose: React + TypeScript
cd your-project
pnpm install
```

---

### ✅ 3. Setup Husky + lint-staged

```bash
pnpm add -D husky lint-staged
pnpm dlx husky-init && pnpm install
```

**Update `.husky/pre-commit`:**

```sh
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

pnpm lint-staged
```

**lint-staged config (`package.json`):**

```json
"lint-staged": {
  "**/*.{ts,tsx,js,jsx}": ["eslint --fix"],
  "**/*.{json,css,md}": ["prettier --write"]
}
```

---

## ▶️ How to Run

```bash
pnpm install     # install dependencies
pnpm dev         # start development server
pnpm lint        # run ESLint
pnpm format      # format code using Prettier
```

---

## 🧠 First-time Git Setup

```bash
git init
pnpm prepare
HUSKY=0 git commit -m "chore: initial commit"
```

---

## 📁 Project Structure

```
.
├── src/                  # Source files
├── public/               # Static files
├── eslint.config.js      # ESLint (Flat config)
├── index.html            # Vite entry point
├── package.json
├── tsconfig.json
├── vite.config.ts
└── .husky/               # Git hooks
```

---

## 📄 License

MIT

---

## 📦 Dependencies

### Runtime

- `react@^19.1.0`
- `react-dom@^19.1.0`

### Dev Dependencies

- `@eslint/js@^9.29.0`
- `@types/react@^19.1.8`
- `@types/react-dom@^19.1.6`
- `@vitejs/plugin-react@^4.5.2`
- `eslint@^9.29.0`
- `eslint-config-prettier@^10.1.5`
- `eslint-plugin-prettier@^5.5.1`
- `eslint-plugin-react-hooks@^5.2.0`
- `eslint-plugin-react-refresh@^0.4.20`
- `globals@^16.2.0`
- `husky@^8.0.0`
- `lint-staged@^16.1.2`
- `prettier@^3.6.2`
- `typescript@~5.8.3`
- `typescript-eslint@^8.34.1`
- `vite@^7.0.0`

> 🛠️ Managed using `pnpm@10.12.4`