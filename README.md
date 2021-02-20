# New Project

> ✨ Bootstrapped with Create Snowpack App (CSA).

## Fix

I've fixed styled-components using [patch-package](https://www.npmjs.com/package/patch-package) to replace ESM module by CJS module into styled-components' package.json.

To do that, I have:

1) manually edited the styled-components package.json to change `jsnext:main` and `module` property to CJS module.
2) Run this command: `npx patch-package styled-components --exclude '\\.js$'`
3) Add `postinstall` hook in my own package.json to run `patch-package` for every install
4) That works 🎉

## Available Scripts

### npm start

Runs the app in the development mode.
Open http://localhost:8080 to view it in the browser.

The page will reload if you make edits.
You will also see any lint errors in the console.

### npm run build

Builds a static copy of your site to the `build/` folder.
Your app is ready to be deployed!

**For the best production performance:** Add a build bundler plugin like "@snowpack/plugin-webpack" to your `snowpack.config.js` config file.

### npm test

Launches the application test runner.
Run with the `--watch` flag (`npm test -- --watch`) to run in interactive watch mode.
