# Create React App [![Build & Test](https://github.com/facebook/create-react-app/actions/workflows/build-and-test.yml/badge.svg?branch=main)](https://github.com/facebook/create-react-app/actions/workflows/build-and-test.yml) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-green.svg)](https://github.com/facebook/create-react-app/blob/main/CONTRIBUTING.md)

<img alt="Logo" align="right" src="https://create-react-app.dev/img/logo.svg" width="20%" />

* goal
  * create React apps / 💡NO build configuration (webpack, Babel, ...)💡
    * Reason: 🧠NO needed, because they are preconfigured 🧠

* use cases
  * **Learning React**
    * | development environment
      * comfortable
      * feature-rich 
  * **Starting NEW SPA React**
  * **Creating examples** -- for your -- libraries and components

* available |
  * macOS,
  * Windows,
  * Linux
  
* questions | [GitHub Discussions](https://github.com/facebook/create-react-app/discussions)

## Creating an App

* requirements
  * Node v14.0.0+ | your local development machine
    * recommendations
      * use
        * the latest LTS version
        * [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows)
          * Reason: 🧠 switch Node versions between different projects 🧠

* recommendations
  * NOT install `create-react-app` globally
    * if you have installed -> uninstall -- via -- `npm uninstall -g create-react-app` or `yarn global remove create-react-app`
    * Reason: 🧠ensure that you ALWAYS use the latest version 🧠

* ways to create a NEW app
  * npx

    ```sh
    npx create-react-app my-app
    ```
    * see
      * [npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) 
      * [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f)
  * npm
    * | v6+

      ```sh
      npm init react-app my-app
      ```
  * yarn
    * | v0.25+
  
      ```sh
      yarn create react-app my-app
      ``` 

* create a directory called `my-app` | current folder
  * skeleton
    ```
    my-app
    ├── README.md
    ├── node_modules
    ├── package.json
    ├── .gitignore
    ├── public
    │   ├── favicon.ico
    │   ├── index.html
    │   └── manifest.json
    └── src
        ├── App.css
        ├── App.js
        ├── App.test.js
        ├── index.css
        ├── index.js
        ├── logo.svg
        └── serviceWorker.js
        └── setupTests.js
    ```

* built-in commands
  * `npm start` or `yarn start`
    * runs the app | development mode
      * hot reload
    * open [http://localhost:3000](http://localhost:3000) / view it | browser
    
<p align='center'>
<img src='https://cdn.jsdelivr.net/gh/marionebl/create-react-app@9f6282671c54f0874afd37a72f6689727b562498/screencast-error.svg' width='600' alt='Build errors'>
</p>

  * `npm test` or `yarn test`
    * runs the test watcher | interactive mode
      * by default, ONLY runs tests related | files changed since the last commit
    * see [testing](https://facebook.github.io/create-react-app/docs/running-tests)
  * `npm run build` or `yarn build`
    * builds the app -- for -- production | `build` folder
      * == bundles React 
        * | production mode
        * / optimizes the build
      * build is minified and the filenames include the hashes
      * -> app is ready to be deployed

## Philosophy

* **1! build dependency**
  * uses webpack, Babel, ESLint, and other amazing projects, BUT provides a cohesive curated experience | them

* **NO Configuration REQUIRED**
  * PRE-configuration | 
    * development
    * production
  * -> you can focus on writing code

* **NO Lock-In**
  * run 1! command / ALL the configuration and build dependencies -- will be moved directly into -- your project

## What’s Included?

* 👀ALL to build a MODERN single-page React app 👀
  * React, JSX, ES6, TypeScript and Flow syntax support
  * Language extras beyond ES6
    * _Example:_ object spread operator
  * Autoprefixed CSS
    * _Example:_ NOT need `-webkit-` or other prefixes
  * fast interactive unit test runner with built-in support for coverage reporting.
  * live development server / warns about common mistakes
  * build script -- to bundle -- JS, CSS, and images for production, hashes and sourcemaps
  * offline-first [service worker](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) + [web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/) / meet ALL [Progressive Web App criteria](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)  
    * if you use `react-scripts@2.0.0` or higher -> service worker is opt-in
  * if you want to update PREVIOUS tools -> ALL based on 1! dependency

* about PREVIOUS tools
  * if you want to see how ALL previous tools fit together -> see [this repo](https://github.com/nitishdayal/cra_closer_look)
  * preconfigured / work in a specific way
  * if your project needs more customization -> ["eject"](https://facebook.github.io/create-react-app/docs/available-scripts#npm-run-eject) & customize it

## Popular Alternatives

* use cases / you MIGHT want to try something else
  * React WITHOUT hundreds of transitive build tool dependencies
  * integrate React code -- with a -- server-side template framework (_Example:_ Rails, Django or Symfony)
  * NOT build a SPA -> use
    * [nwb](https://github.com/insin/nwb)
    * [Neutrino](https://neutrino.js.org/)
    * | Rails, use [Rails Webpacker](https://github.com/rails/webpacker)
    * | Symfony, use [Symfony's webpack Encore](https://symfony.com/doc/current/frontend/encore/reactjs.html)
  * publish a React component -> use
    * [nwb](https://github.com/insin/nwb) can [also do this](https://github.com/insin/nwb#react-components-and-libraries)
    * [Neutrino's react-components preset](https://neutrino.js.org/packages/react-components/)
  * server rendering / React and Node.js
    * 👀Create React App is agnostic of the backend 👀
      * == ONLY produces static HTML/JS/CSS bundles
    * -> use
      * [Next.js](https://nextjs.org/) or
      * [Razzle](https://github.com/jaredpalmer/razzle)
  * website MOSTLY static (_Example:_ portfolio or a blog) -> use
    * [Gatsby](https://www.gatsbyjs.org/) or
      * Reason: 🧠 website -- is pre-rendered into -- HTML | build time 🧠
    * [Next.js](https://nextjs.org/) 
      * Reason: 🧠Next.js supports both server rendering and pre-rendering 🧠
  * if you need MORE customization -> see
    * [Neutrino](https://neutrino.js.org/)
      * its [React preset](https://neutrino.js.org/packages/react/)

## React Native

* == [Expo CLI](https://github.com/expo/expo-cli)

## License

* open source software [licensed as MIT](https://github.com/facebook/create-react-app/blob/main/LICENSE)
