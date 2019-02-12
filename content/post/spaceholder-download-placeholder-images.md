+++
title = "Spaceholder: Download placeholder images from public domain sources"
description = "Spaceholder makes it easy to download placeholder images when you need them. Images are downloaded from LoremPixel.com, Placehold.it, PlaceIMG.com, Dummyimage.com"
date = "2016-02-27"
+++

<form name="contact" netlify>
  <p>
    <label>Name <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Email <input type="email" name="email" /></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

I've created a small npm module that makes it easy to download placeholder images from public domain sources.

[See on Github](https://github.com/ecrmnn/spaceholder)

[See on npm](https://npmjs.com/spaceholder)

### Installing
```bash
npm install -g spaceholder
```

### Usage
```bash
spaceholder
# Downloads 1 image (1024x768px) into current directory


spaceholder -n 100
# Downloads 100 images into current directory


spaceholder -s 800x600
# Downloads 1 image (800x600px) into current directory


spaceholder -n 50 -s 800x600 -p LoremPixel
# Downloads 50 images (800x600px) from LoremPixel into current directory
# If no --provider / -p is specified, each image is downloaded from a random provider
```