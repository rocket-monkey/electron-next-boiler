# electron-next-boiler

This is a minimal Electron application based on this [Repository](https://github.com/electron/electron-quick-start). To get more detail, read this [Quick Start Guide](https://electronjs.org/docs/tutorial/quick-start) within the Electron documentation.

## How To

- clone this repository
- cd into it and run `yarn`
- run `yarn start` to run the app in dev mode
- run `yarn dist` to build the app for your current platform

## How to develop

so the initial structure given in the boilderplate is:

```
main
 ├──index.js                              * the main process of the electron app
renderer                                  * our custom renderer solved with next.js
 ├──pages/                                * the routing in next.js is done with these "pages"
 |    ├──start.js                         * the entry point into our app, the "first page"
 |    └──...                              * more pages/routes you will define in the future
 ├──next.config.js                        * the main config for next.js, used to utilize webpack
src                                       * the source folder of our react application - this part is isomorphic, could be rendererd everywhere
 ├──@core/                                * one of our aliases for easy import paths, the core components
 |    ├──layout                           * the entry point into our app, the "first page"
 |    |    └──index.js                    * the core layout component, defining the layout around all our react pages
 |    └──...                              * more core react components
 ├──@sites/                               * the next aliase for easy import paths, the sites components
 |    ├──home                             * the entry point into our app, the "first page"
 |    |    └──index.js                    * the first real site/route of the app, Home
 |    └──...                              * more sites/routes solved as react components

```

### Specialities

- the app has already defined a [frameless window](https://github.com/electron/electron/blob/master/docs/api/frameless-window.md), a drag area and dark background color 😎

## What's inside

- next.js renderer setup (like you know it from next)
- react 16 and es6 support with babel
- nice dev workflow with HMR (live code pushing into the app on save)
- styled-jsx support for a styling solution that also works in the production build of the app
- a nice project structure done with alias definitions in babel and webpack (see next.config.js)
