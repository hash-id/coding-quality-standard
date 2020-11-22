[![js-semistandard-style](https://raw.githubusercontent.com/standard/semistandard/master/badge.svg)](https://github.com/standard/semistandard)

## VSCode Plugins

### Recommended

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=visualstudioexptteam.vscodeintellicode)
- [gitflow](https://marketplace.visualstudio.com/items?itemName=vector-of-bool.gitflow)
- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
- [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)

### Nice to Have

- [GraphQL for VSCode](https://marketplace.visualstudio.com/items?itemName=kumar-harsh.graphql-for-vscode)
- [Inline Bookmarks](https://marketplace.visualstudio.com/items?itemName=tintinweb.vscode-inline-bookmarks)
- [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
- [Polacode](https://marketplace.visualstudio.com/items?itemName=pnp.polacode)

## Linter

Install ESLint and prettier-related dependencies on current project

```
npm install -D eslint eslint-config-prettier eslint-plugin-prettier
```

> for Yarn, use `yarn add --dev` as an alternative

run the ESLint wizard

```
./node_modules/.bin/eslint --init
```

Wizard guidelines:

1. Pick `To check syntax, find problems, and enforce code style`
2. Use `JavaScript modules` for Typescript project, OR `CommonJS` for Javascript project
3. Use `None of These` for NodeJS project, OR `React` for React project
4. For Typescript project, please pick `Yes`
5. Pick `Browser` for React project, otherwise `Node`
6. Pick `Use a popular style guide`, and choose `Standard`
7. Pick `JavaScript` as the config file format
8. You will be prompted to install several eslint dependencies, please answer with `Yes` or `Y`

## Prettier

Install prettier in your project and pin its version

```
npm install prettier -D --save-exact
```

### Create `.prettierrc` file on project root folder.

```json
{
  "tabWidth": 2,
  "useTabs": false,
  "printWidth": 100,
  "singleQuote": true,
  "semi": true
}
```

### Modify your current `.eslintrc.js`

1. Add `prettier` as plugins
2. Append `plugin:prettier/recommended` on extends

```js
// example
{
  plugins: ['prettier'],
  extends: ['standard', 'plugin:prettier/recommended'],
}
```

### Configure VSCode plugin

Please install `vscode prettier plugin` and configure your default formatter.

1. Open `Settings`
2. Type `Default formatter` in search bar
3. Pick `esbenp.prettier-vscode` as default formatter and save your setting
