# lit-tailwind-cypress-storybook

This repo contains a simple rating app with the following products:

- lit
- TailwindCSS
- Cypress.io
- Storybook

It serves as a reproduction sample for the follwoing vite-generated warning since version 4.
The warning is reported [here](https://github.com/vitejs/vite/issues/11350).

```
[vite] warning:
/Users/patrickineichen/Git/create-vite-ts-playground/lit-tailwind-cypress-storybook/src/tailwind.ts
1  |  import { adoptStyles, LitElement, unsafeCSS } from "lit";
2  |  import style from "./tailwind.css";
   |                     ^
3  |  export class TwLitElement extends LitElement {
4  |    connectedCallback() {
Default and named imports from CSS files are deprecated. Use the ?inline query instead. For example: import style from "./tailwind.css?inline"
  Plugin: vite:import-analysis
  File: /Users/patrickineichen/Git/create-vite-ts-playground/lit-tailwind-cypress-storybook/src/tailwind.ts
```

How to reproduce:
- `npm run storybook`
