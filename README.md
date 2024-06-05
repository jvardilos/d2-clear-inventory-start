# Destiny 2 Inventory Clearer (research app)

* pre-production, I'm building this app cleaner later, but this is the first attempt

## Running

* dev build

  ``` bash
  yarn
  yarn run dev
  ```

* build production ready build

  ``` bash
  yarn run build
  ```

* run that production ready build

  ``` bash
  yarn run preview
  ```

* TODO: make this a docker task so I can put this in ECS

## Dev env set up

* Requirements
  * Ubuntu

* install nvm

  ``` bash
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
  nvm install node
  ```

* install yarn

  ``` bash
  npm install yarn --global
  ```

* cd and yarn

  ``` bash
  cd d2-clear-inventory
  yarn
  ```

## TODO: provide a launch json

## TODO: OTHER NOTES ON VITE BUILD BELOW

## React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default {
  // other rules...
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
  },
}
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list
