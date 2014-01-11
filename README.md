# process

```require('process');``` just like any other module.

Works in node.js and browsers via the browser.js shim provided with the module.

## browser implementation

The goal of this module is not to be a full-fledged alternative to the builtin process module. This module mostly exists to provide the nextTick functionality and nothing more. We keep this module lean because it will often be included by default by tools like browserify when it detects a module has used the `process` global.

If you are looking to provide other process methods, I suggest you monkey patch them onto the process global in your app.

## package manager notes

If you are writing a bundler to package modules for client side use, make sure you use the ```browser``` field hint in package.json.

See https://gist.github.com/4339901 for details.

The [browserify](https://github.com/substack/node-browserify) module will properly handle this field when bundling your files.


