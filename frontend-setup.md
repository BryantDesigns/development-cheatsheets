# Tailwind CSS Setup with Vite and React

This guide provides a step-by-step process to set up a React project with Vite and integrate Tailwind CSS, along with some useful plugins and configurations.
https://tailwindcss.com/docs/guides/vite

## Create Vite Project

First, create a new Vite project with a React template by running the following command:

```bash
npm create vite@latest ./ -- --template react
```

## Tailwind Setup
Install Tailwind CSS and initiate its configuration:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
To use Tailwind with some common UI components and icons, install Headless UI and Heroicons:


```bash
npm install @headlessui/react@latest
npm install @heroicons/react@latest
```
## Tailwind Plugins
Enhance Tailwind CSS with additional plugins for typography, container queries, forms, and aspect ratio support:

```bash
npm install -D @tailwindcss/typography
npm install -D @tailwindcss/container-queries
npm install -D @tailwindcss/forms
npm install -D @tailwindcss/aspect-ratio
```
## Update `tailwind.config.js`
Include the installed plugins in your Tailwind configuration:


```bash
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
    plugins: [
    require("@tailwindcss/typography"),
    require("@tailwindcss/aspect-ratio"),
    require("@tailwindcss/container-queries"),
    require("@tailwindcss/forms"),
  ],
}
```
## Code Formatting with Prettier
For better code formatting, especially with Tailwind CSS, install Prettier and its Tailwind CSS plugin:



```bash
npm install -D prettier prettier-plugin-tailwindcss
```
### Configure Prettier
Create a Prettier configuration file to customize its behavior:


```bash
// prettier.config.js, .prettierrc.js, prettier.config.cjs, or .prettierrc.cjs

/** @type {import("prettier").Config} */
const config = {
  trailingComma: "es5",
  tabWidth: 4,
  semi: false,
  singleQuote: true,
  plugins: ['prettier-plugin-tailwindcss'],
};

module.exports = config;

```
