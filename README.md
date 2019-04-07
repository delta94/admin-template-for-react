# Admin Template for React

[DEMO](https://admin-react.bndy.net/) - username: **test**, password: **test**

[![Netlify Status](https://api.netlify.com/api/v1/badges/f1d6e125-33e2-42a7-a97e-67a912d878af/deploy-status)](https://app.netlify.com/sites/admin-react/deploys)
![](https://img.shields.io/badge/Language-TypeScript-blue.svg)
![](https://img.shields.io/badge/Language-SCSS-blue.svg)
![](https://img.shields.io/badge/React-16.3-brightgreen.svg?logo=react)
![](https://img.shields.io/badge/React-Redux-brightgreen.svg?logo=react)
![](https://img.shields.io/badge/React-react--router--config-brightgreen.svg?logo=react)
![](https://img.shields.io/badge/React-react--intl-brightgreen.svg?logo=react)
![](https://img.shields.io/badge/React-connected--react--router-brightgreen.svg?logo=react)
![](https://img.shields.io/badge/React-Redux%20Saga-brightgreen.svg?logo=react)
[![code style: prettier](https://img.shields.io/badge/Code_Style-Prettier-ff69b4.svg)](https://github.com/prettier/prettier)


A starter admin template with React, React Redux, Material UI and TypeScript that packages using Webpack and integrates a minimal project structure.

![](https://raw.githubusercontent.com/bndynet/admin-template-for-react/master/docs/images/admin-home.png)

- AJAX component: **[axios](https://github.com/axios/axios)**
- UI component: **[material-ui](https://material-ui.com/)**
- REACT stack: react, react-dom, react-redux, react-router-config, react-router-dom, redux, redux-saga

## Getting Started

1. Clone repo `git clone <git-url>`
2. `npm install` to install all dependencies
3. `npm start` to start web server
4. `npm run build` to build production code into **dist** folder

## Development

### Application Configuration Examples

- ./src/config/app.common.tsx           - *all common configurations*
- ./src/config/app.dev.tsx              - *configurations used in local*
- ./src/config/app.prod.tsx             - *configurations used in production*
- ./src/config/app.github.tsx           - *example for github authorization*
- ./src/config/app.auth-code.tsx        - *example for authorization code grant type*
- ./src/config/app.auth-password.tsx    - *example for password grant type*

### Customize more environments

1. New file **./src/config/app.[env_name].tsx** to override your configurations

2. Recommend to import configurations in **app.dev.tsx**

    ```ts
    import config = require("./app.your-env");
    ```

    Or add below code in **./src/config/index.tsx** or **./index.html** to freeze your environment

    ```ts
    window.__APP_ENV__ = 'your-env';
    ```

3. `npm start` and `npm run build` will always use the environment you defined

### Components based on Material UI or some else

`Alert`, `Loading`, `MiniCard`, `Notifier`, `Overlay`, `Panel`, `Tag`, ...

### i18n/l10n Support

```tsx
<Formatter i18nKey='hi' value={{name: 'Bendy'}} description='This is a welcome message.' descriptionPlacement='top' />

<Formatter value={10000} />

<Formatter value={1459832991883} formatAs='date' />

<Formatter value={1459832991883} formatAs='time' />

<Formatter value={1459832991883} formatAs='fromNow' />
```

### Debug with **Chrome** in **Visual Studio Code**

1. Requires **[Visual Studio Code](https://code.visualstudio.com/)** as IDE and extension **[Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)**

1. `npm start` to run application

1. Click menu **Debug** > **Start Debugging** to debug with generated **.vscode/launch.json** file as below:

    ```json
    {
        "version": "0.2.0",
        "configurations": [
            {
                "type": "chrome",
                "request": "launch",
                "name": "Launch Chrome against localhost",
                "url": "http://localhost:8080",
                "webRoot": "${workspaceFolder}"
            }
        ]
    }
    ```

1. Set breakpoints in your **vscode** and operate in the new Chrome window **Start Debugging** opened

### Recommendatory extensions for **Chrome**

- React Developer Tools
- Redux DevTools

Above extensions will show you the **Actions**, **States** and **Reducers** in **Chrome** console.