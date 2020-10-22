# React-Static - Basic Template

To use this template, run `react-static create` and use the `basic` template.

## Steps

- Install packages
  - `preact`
  - `@prefresh/webpack`
  - `patch-package`
- Add **postinstall** script to `patch-package`
- Create a new patch to delete Suspense lines in `node_modules/react-static/src/bootstrapApp.js` (patch is in `patches/react-static+7.4.2.patch`)
- Create the `react-static-plugin-preact` from [react-static](https://github.com/react-static/react-static/blob/master/packages/react-static-plugin-preact/src/node.api.js) (not published yet) and add it to `static.config.js` plugins
- Remove `<Suspense />` around `<Comp />` in `src/index.js`

## What is wrong?

- `yarn start` runs perfectly
- `yarn build && yarn serve` shows error `Cannot set property Suspense of #<Object> which has only a getter`