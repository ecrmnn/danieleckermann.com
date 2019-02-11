+++
title = "How to bundle Twitter Bootstrap with Laravel Mix"
description = "Getting Bootstrap to work with a module bundler is a nightmare. With Laravel Mix's autoload feature, it's a breeze"
date = "2017-05-14"
+++

Getting Bootstrap to work with a module bundler is a nightmare.

I've tried a hundred times, but I always end up debugging some of Bootstraps requirements before getting it to work.

This short guide will probably help me many times in the future, and hopefully you'll get something out of it too.

### Install required modules
```bash
npm install bootstrap
npm install jquery
npm install tether
```

### Configure your ``webpack.mix.js`` file
``mix.autoload`` does all the work for us here. Exposing jQuery and Tether in the ``window``-scope.
```js
// webpack.mix.js

const { mix } = require('laravel-mix');

mix.autoload({
  jquery: ['$', 'jQuery', 'window.jQuery'],
  tether: ['Tether', 'windows.Tether']
});

mix.sass('resources/assets/sass/app.scss', 'public/css');
mix.js('resources/assets/js/app.js', 'public/js');

```

### Require / Import bootstrap in your main JS-file
We're using ES6 syntax here, but you can use ``require()`` if you want.
```js
// app.js

import '../../../node_modules/bootstrap/dist/js/bootstrap';
```


### Ready, set, go
Now you're ready to compile your assets
```bash
npm run dev
```