+++
title = "Electron: Prevent dropped file from opening in window"
description = "How to prevent Electron from opening a dropped file in the app window"
date = "2016-03-01"
+++

When building an Electron app you're able to drag files into the app and get redirected to that file.

#### TLDR?
I've created a NPM package to fix this issue.
You can check it out here ([ecrmnn/electron-disable-file-drop](https://github.com/ecrmnn/electron-disable-file-drop))


E.g. if you drag an image from your desktop into the app, you'll get redirected to the image - just as if you dragged an image into Chrome.

There is an easy way to fix this by adding the following

```javascript
'use strict';

document.addEventListener('dragover', function (event) {
  event.preventDefault();
  return false;
}, false);

document.addEventListener('drop', function (event) {
  event.preventDefault();
  return false;
}, false);
```