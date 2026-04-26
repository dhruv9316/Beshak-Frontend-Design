# Beshak frontend design

Vue 3 + TypeScript + Vite + Tailwind CSS. Development uses `<script setup>` and the Vue 3 SFC model.

## Prerequisites

- [Node.js](https://nodejs.org/) **20 LTS or newer** (includes `npm`)
- A Git client if you are cloning the repository

## Local setup

1. **Clone the repository** and open the project root
2. **Install dependencies** (use one package manager; `npm` is the default in this project):
  ```bash
   npm install
  ```
3. **Start the dev server** (hot-reload, default URL in the terminal):
  ```bash
   npm run dev
  ```
   Vite will print a local address such as `http://localhost:5173`. Open it in your browser.

## Other scripts


| Command           | Description                                     |
| ----------------- | ----------------------------------------------- |
| `npm run build`   | Typecheck (`vue-tsc`) and production Vite build |
| `npm run preview` | Local preview of the production build output    |


## Editor tips (optional)

- [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) for VS Code: syntax, TypeScript, and SFC support.

## Learn more

- [Vite](https://vite.dev/)
- [Vue 3](https://vuejs.org/) · [TypeScript in Vue](https://vuejs.org/guide/typescript/overview.html)
- [Tailwind CSS](https://tailwindcss.com/docs)

