# Destiny 2 Inventory Clearer (research app)

* pre-production, I'm building this app cleaner later, but this is the first attempt

## Dev env set up

* Requirements
  * Ubuntu
  * VScode
  * TODO: I will make this more flexible in the future, but a launch json will be in my requirements for now

* Install nvm

  ``` bash
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
  nvm install node
  ```

* Install yarn

  ``` bash
  npm install yarn --global
  ```

* cd and yarn

  ``` bash
  cd d2-clear-inventory
  yarn
  ```

* Create this launch.json, replace "program" value with your PATH to your yarn binary

``` bash
# to find your yarn PATH
which yarn
```

``` json
{
    "version": "0.2.0",
    "configurations": [
      {
        "name": "Yarn Run Dev",
        "type": "node",
        "request": "launch",
        "program": "~/.nvm/versions/node/v22.2.0/bin/yarn",
        "args": ["run", "dev"],
        "cwd": "${workspaceFolder}",
        "console": "integratedTerminal"
      },
      {
        "name": "Yarn Run Build",
        "type": "node",
        "request": "launch",
        "program": "~/.nvm/versions/node/v22.2.0/bin/yarn",
        "args": ["run", "build"],
        "cwd": "${workspaceFolder}",
        "console": "integratedTerminal"
      },
      {
        "name": "Yarn Run Preview",
        "type": "node",
        "request": "launch",
        "program": "~/.nvm/versions/node/v22.2.0/bin/yarn",
        "args": ["run", "preview"],
        "cwd": "${workspaceFolder}",
        "console": "integratedTerminal"
      }
    ]
  }
```

* With this in place,

## TODO: OTHER NOTES ON VITE BUILD BELOW

## React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

* [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
* [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

* Configure the top-level `parserOptions` property like this:

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

* Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
* Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
* Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list
