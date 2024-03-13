https://tailwindcss.com/docs/guides/vite
npm create vite@latest ./ -- --template react

## Tailwind Setup
npm install -D tailwindcss
npx tailwindcss init

npm install @headlessui/react@latest
npm install @heroicons/react@latest



## Tailwind Plugins
npm install -D @tailwindcss/typography
npm install -D @tailwindcss/container-queries
npm install -D @tailwindcss/forms
npm install -D @tailwindcss/aspect-ratio

### Add this to tailwind.config.js
plugins: [
        require("@tailwindcss/typography"),
        require("@tailwindcss/aspect-ratio"),
        require("@tailwindcss/container-queries"),
        require("@tailwindcss/forms"),
]

npm install -D prettier prettier-plugin-tailwindcss



### prettier.config.js
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
