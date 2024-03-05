# Create Awesome React Application

> Opinionated React starter template using TypeScript, Redux, React Router, Redux Saga, SCSS, PostCSS and more, offering PWA and offline capabilities and many more.

## Dependencies

In order to use this setup you need to have installed the following dependencies:

1.  Node - min v8.15.0
2.  NPM - min v5.6.0
    or
3.  Yarn - min v1.3.2

## One line zero config installation

## Install

```sh
yarn

# or

npm i
```

## Develop

```sh
yarn start

# or

npm start
```

## Build

```sh
yarn build

# or

npm run build
```

## Lint

```sh
yarn lint

# or

npm run lint
```

## Test

```sh
yarn test

# or

npm run test
```

## Details

1.  Folder structure:

    ```
    📦 project
    ┣ 📂 assets - all fonts, images, videos, translation files, etc
    ┣ ┣ 📂 locale - all translations
    ┣ ┣ 📂 styles - all shared stylesheets
    ┃ ┃ ┗ 📜 app.scss - Application's global SCSS entry point
    ┃ ┃ ┗ 📜 mixins.scss - Application's SCSS mixins
    ┃ ┃ ┗ 📜 functions.scss - Application's SCSS functions
    ┃ ┃ ┗ 📜 settings.scss - Application's SCSS settings (variables, etc)
    ┣ 📂 components - stateless components
    ┣ 📂 containers - statefull components. Each container can export more than one component. An example folder structure is included in (`src/containers/.boilerplate`)
    ┣ 📂 i18n - configuration settings for i18n (internationalization)
    ┣ 📂 store - The application Redux store
    ┣ ┣ 📂 branches - all store branches
    ┣ ┣	┣ ┣ 📂 $BRANCH - A branch in the Redux store
    ┃ ┃ ┃ ┗ 📜 enums.ts - Each branch has its own enums
    ┃ ┃ ┃ ┗ 📜 interfaces.ts - Each branch has its own interfaces
    ┃ ┃ ┃ ┗ 📜 reducer.ts - The branch reducer
    ┃ ┃ ┃ ┗ 📜 selectors.ts - The branch selectors (hooks)
    ┃ ┃ ┃ ┗ 📜 sagas.ts - The branch sagas
    ┃ ┗ 📜 enums.ts - Store's enums
    ┃ ┗ 📜 index.ts - Application's main store
    ┃ ┗ 📜 interfaces.ts - Store's interfaces
    ┃ ┗ 📜 root-reducer.ts - Application's root reducer
    ┃ ┗ 📜 sagas.ts - Application's sagas
    ┣ 📂 utilities - helpers and utility functions
    ┗ 📜 app.tsx - Application's main component
    ┗ 📜 custom.d.ts - Custom type definitions
    ┗ 📜 index.html - Application's HTML file
    ┗ 📜 index.tsx - The main entry point
    ┗ 📜 loadables.tsx - Code split and lazy loaded components
    ```

2.  Latest EcmaScript support

    -   Usage of the latest features in EcmaScript
    -   Using [TypeScript](https://www.typescriptlang.org/) to transpile to ES5
    -   Minification of the bundled file
    -   Source maps

3.  Aliases: Checkout the aliases property in the `vite.config.ts` and `tsconfig.json` files.
4.  SCSS usage.
5.  Lint your files: ESLint (with TypeScript ESLint installed and configured) and Stylelint included
6.  Tests using Jest and React testing library. The Test environment has been configured so you don't have to
7.  PWA ready - Install as a native app on Android and iOS
8.  Code splitting and lazy loading
9.  i18n included:
    1.  add your locales in `/src/i18n/locales`
    2.  add your po files which are based on the `translations.pot` file located in `/src/assets/locale`
    3.  run `yarn locale` to generate `${locale}.json` file from your `${locale}.po` file.
    4.  update your UI to reflect the newly added locale
10. Prerendering - All pages are prerendered based on defined routes. This is included in the build step and needs **no additional configuration**.

## Supported Browsers

This setup uses [Browserslist](https://github.com/browserslist/browserslist) to target browsers.

The default list of supported browsers is listed in the `package.json` file:

```json
{
	"browserslist": ["> 1%", "last 2 versions"]
}
```

This means that supported browsers vary based on current usage data and current browser versions.

In general, this setup supports the two most recent versions of all browsers.

## Added auth

The start template contains a ready-to-use auth flow with Login, Logout, Sign up and Forgotten password forms with validation included. The auth flow includes also route guarding and redirects based on auth status. Please take a look at the `/src/containers/auth` folder for more details.

The starting files also include ready-to-use layout components such as `Header`, `Footer`, `Wrapper`, `Button`, `Icon` and form `Field`s.


## Dependencies
 
@loadable/component:
Purpose: Allows you to split your code into separate bundles which can be loaded on demand, improving the performance of your application by reducing initial load times.
Usage: It's commonly used in React applications where you want to dynamically load components only when they're needed, instead of loading them all upfront.

@redux-devtools/extension:
Purpose: Provides a set of developer tools to help you debug and monitor the state and behavior of your Redux application.
Usage: Typically used during development to inspect the state changes, action history, and performance of Redux applications directly in the browser's developer tools.

axios:
Purpose: A promise-based HTTP client for making asynchronous HTTP requests from JavaScript applications.
Usage: Often used in React applications to communicate with backend servers or APIs, fetching data and sending requests.

date-fns:
Purpose: A library for manipulating and formatting dates in JavaScript, providing a wide range of functions for common date-related tasks.
Usage: Useful for handling dates and times in React applications, including parsing, formatting, comparing, and manipulating dates.

i18next:
Purpose: A comprehensive internationalization (i18n) library for JavaScript, providing tools for managing translations, pluralization, formatting, and more.
Usage: Used to implement multi-language support in React applications, allowing you to easily localize your user interface and handle translations.

i18next-browser-languagedetector:
Purpose: A plugin for i18next that automatically detects and sets the language of the user's browser, making it easier to provide localized content.
Usage: Typically used alongside i18next to automatically detect the user's preferred language and load the appropriate translations.

normalize.css:
Purpose: A CSS reset library that normalizes styles across different web browsers, ensuring consistent rendering and behavior.
Usage: Included in React projects to reset default browser styles and provide a clean foundation for styling components.

react and react-dom:
Purpose: The core React libraries for building user interfaces in JavaScript applications and rendering React components into the DOM.
Usage: Essential for building React applications, providing the foundational elements for creating components, managing state, and handling UI rendering.

react-hook-form:
Purpose: A library for managing form state in React applications using hooks, providing a simpler and more efficient alternative to traditional form management libraries.
Usage: Used to handle form validation, submission, and state management in React applications, improving performance and developer experience.

react-i18next:
Purpose: React bindings for i18next, making it easier to integrate the i18next internationalization library with React applications.
Usage: Simplifies the process of using i18next in React components, providing hooks and components for handling translations and language switching.

react-inlinesvg:
Purpose: A library for rendering inline SVGs directly in React components, allowing you to include SVG files as components in your JSX code.
Usage: Useful for working with SVG images in React applications, providing a convenient way to use SVGs with the benefits of React's component-based architecture.

react-redux:
Purpose: Official React bindings for Redux, enabling seamless integration of Redux state management with React components.
Usage: Used to connect React components to the Redux store, allowing them to access state and dispatch actions to update the state.

react-router and react-router-dom:
Purpose: Libraries for managing routing and navigation in React applications, enabling declarative routing and dynamic rendering of components based on URL changes.
Usage: Essential for building single-page applications (SPAs) with React, providing navigation between different views and handling routing logic.

redux:
Purpose: A predictable state container for JavaScript applications, providing a centralized store for managing application state and state changes.
Usage: Commonly used in React applications to manage complex state logic, allowing components to access and update state in a predictable and maintainable way.

redux-saga:
Purpose: A library for managing side effects, such as asynchronous operations and handling of impure actions, in Redux applications.
Usage: Used alongside Redux to encapsulate side effects in a separate layer, improving testability and maintainability of Redux applications.

scss-goodies:
Purpose: A collection of SCSS mixins and functions that provide utility and convenience when writing SCSS stylesheets.
Usage: Helps streamline SCSS development in React projects, providing reusable mixins and functions for common styling tasks and patterns.

