---
id: getting-started
title: Getting Started
---

* Create React App
  * == way to create single-page React applications /
    * officially supported
    * modern build setup WITHOUT configuration

## Quick Start

* recommendations
    * `npm uninstall -g create-react-app` / `yarn global remove create-react-app`
        * == uninstall the global package installed
        * Reason: 🧠 ensure that LATEST version is used 🧠
* 
    ```sh
    npx create-react-app my-app
    cd my-app
    npm start
    ```
* | your browser,
  * [http://localhost:3000/](http://localhost:3000/)
* if you’re ready to deploy | production -> run `npm run build`
  * Reason: 🧠create a minified bundle 🧠 

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/facebook/create-react-app@27b42ac7efa018f2541153ab30d63180f5fa39e0/screencast.svg' width='600' alt='npm start' />
</p>

### Get Started Immediately

* NOT need to install or configure tools (webpack nor Babel)
  * Reason: 🧠They are preconfigured and hidden🧠

## Creating an App

* requirements
  * 👀Node v14+ | your local development machine (NOT required | server) 👀

* methods -- to -- create the app

### npx

```sh
npx create-react-app@latest my-app
```

* [npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)
  * built-in with npm v5.2+

### npm

```sh
npm init react-app my-app
```

* npm v6+

### Yarn

```sh
yarn create react-app my-app
```

* Yarn v0.25+

### Selecting a template

* `--template [template-name]`
  * optional command's option
  * == `npx create-react-app my-app --template [template-name]` 

* `cra-template-[template-name]`
  * templates name format

* [list of available templates](https://www.npmjs.com/search?q=cra-template-*)
* see [custom Templates](custom-templates.md)

#### Creating a TypeScript app

* if you want to create a NEW TypeScript app -> use `--template typescript`

    ```sh
    npx create-react-app my-app --template typescript
    ```

* if you want to add TypeScript | EXISTING project -> see [Adding TypeScript](adding-typescript.md)

## Output

* `my-app/` 

    ```
    my-app
    ├── README.md
    ├── node_modules
    ├── package.json
    ├── .gitignore
    ├── public
    │   ├── favicon.ico
    │   ├── index.html
    │   ├── logo192.png
    │   ├── logo512.png
    │   ├── manifest.json
    │   └── robots.txt
    └── src
        ├── App.css
        ├── App.js
        ├── App.test.js
        ├── index.css
        ├── index.js
        ├── logo.svg
        ├── serviceWorker.js
        └── setupTests.js
    ```

## Scripts

* | AFTER creating the project,
  * built-in scripts

### `npm start` or `yarn start`

* runs the app in development mode
  * == if you make changes -> HOT reload
* | browser, open [http://localhost:3000](http://localhost:3000)

<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/marionebl/create-react-app@9f6282671c54f0874afd37a72f6689727b562498/screencast-error.svg' width='600' alt='Build errors' />
</p>

### `npm test` or `yarn test`

* runs the test watcher in an interactive mode

* see [testing](running-tests.md)

### `npm run build` or `yarn build`

* builds the app -- for -- production | `build/`
  * == bundles React
    * in production mode
    * / 
      * optimizes the build
      * build is minified
      * filenames include the hashes
