# yet-another-vscode-extension-pack

This extension pack adds features to make my life easier while working with VSCode.

## Note

**Please read & follow the [Recommended Settings](#Recommended-Settings) section to enable all features.**

## Recommended-Settings

### Setup VS Code

Enable FormatOnSave & ESLint for `.js` and `.vue` files in VS Code settings:

```js
// enable autofix for Vue files

{
  "eslint.enable": true,
  "eslint.alwaysShowStatus": true,
  "eslint.validate": [
    "javascript",
    {
      "language": "vue",
      "autoFix": true
    },
    {
      "language": "html",
      "autoFix": true
    }
  ],
  "eslint.options": {
    "extensions": [".js", ".vue"]
  }
}

```

### Setup ESLint

- Install following packages:

```bash
npm i -D \
    eslint \
    eslint-config-airbnb-base \
    eslint-config-contaazul \
    eslint-config-prettier \
    eslint-plugin-vue \
    eslint-plugin-prettier \
    @vue/cli-plugin-eslint \
    @vue/eslint-config-prettier \
    prettier \
    prettier-eslint \
    babel-eslint
```

- Create/update ESLint config file (`package.json`, `.eslintrc.js` or `.eslintrc.json`) in your project folder:

```js
// config ESLint and Prettier to work with Vue

module.exports = {
  root: true,
  parserOptions: {
    parser: 'babel-eslint'
  },
  plugins: [
    'prettier',
    'vue',
  ],
  extends: [
    'plugin:vue/recommended',
    'prettier',
    'prettier/vue',
    'contaazul',
  ],
  rules: {
    'prettier/prettier': 'error',
  },
};
```

## Extensions Included in this pack

- [Auto-Close-Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag) -
  Automatically add HTML/XML close tag, same as Visual Studio IDE or Sublime Text
- [Auto-Rename-Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) -
  Auto rename paired HTML/XML tag
- [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments) -
  Improve your code commenting by annotating with alert, informational, TODOs, and more!
- [Bracket Pair Colorizer](https://marketplace.visualstudio.com/items?itemName=coenraads.bracket-pair-colorizer) -
  A customizable extension for colorizing matching brackets
- [CodeMetrics](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics) -
  Computes complexity in TypeScript / JavaScript files.
- [EditorConfig](https://marketplace.visualstudio.com/items?itemName=editorconfig.editorconfig) -
  EditorConfig Support for Visual Studio Code
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) -
  Integrates ESLint into VS Code.
- [Formatting Toggle](https://marketplace.visualstudio.com/items?itemName=tombonnike.vscode-status-bar-format-toggle) -
  A VS Code extension that allows you to toggle the formatter on and off with a simple click
- [GitLens](https://marketplace.visualstudio.com/items?itemName=robertoachar.vscode-essentials-snippets) -
  Supercharge the Git capabilities built into Visual Studio Code
- [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost) -
  Display import/require package size in the editor
- [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow) -
  Makes indentation easier to read
- [JavaScript (ES6) Snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets) -
  Code snippets for JavaScript in ES6 syntax
- [Jest](https://marketplace.visualstudio.com/items?itemName=orta.vscode-jest) -
  Use Facebook's Jest With Pleasure.
- [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script) -
  npm support for VS Code
- [npm IntelliSense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense) -
  Visual Studio Code plugin that autocompletes npm modules in import statements
- [Path IntelliSense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) -
  Visual Studio Code plugin that autocompletes filenames
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) -
  VS Code plugin for prettier/prettier
- [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur) -
  Vue tooling for VSCode
- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons) -
  Icons for Visual Studio Code

## Credits

All credits goes to original authors of the above mentioned extensions.

**Happy Coding!**
