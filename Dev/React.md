Installation:

# React with Vite

```
npm create vite@latest
```

Alternative:

```
npm create vite@latest Project_Name -- --template react
```

## Tailwind in React-Vite

- Installation

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

- Path Configuration

```
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

- Adding Tailwind Directives

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### One-Liner(React + Tailwind)
```
npm create vite@latest my-project --template react && cd my-project && npm install -D tailwindcss postcss autoprefixer && npx tailwindcss init -p

```


### Links

- [React Docs](https://react.dev/learn)
- [Tailwind Docs](https://tailwindcss.com/docs/installation)
- [React-Router](https://reactrouter.com/en/main)

## Using Pnpm:

Pnpm is an alternative to npm which is faster than npm.


```
pnpm create vite project_name
```

## One-Liner to create Vite with Tailwind using pnpm

```
pnpm create vite@latest my-project --template react && cd my-project && pnpm install -D tailwindcss postcss autoprefixer && npx tailwindcss init -p
```


