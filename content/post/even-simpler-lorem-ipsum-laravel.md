+++
title = "Lorem: Dummy text and images for Laravel"
description = "Sick of copying and pasting lorem ipsum text and placeholder images? Lorem can help you"
date = "2016-03-03"
+++

Adding lorem ipsum text and placeholder images for the millionth time?

I've created a super small Laravel package for making this boring task a little less annoying.

### Install
```bash
composer require ecrmnn/lorem
```

After you have installed open your Laravel config file ``config/app.php`` and add the following lines.
In the $providers array add the service providers for this package.
```php
Ecrmnn\Lorem\LoremServiceProvider::class
```

### Usage
Access ``Lorem`` by using the global helper ``lorem()``

#### Text
```html
<body>
    <div class="content">
        <!-- Returns one paragraph of lorem ipsum -->
        {!! lorem(1) !!}
    </div>
</body>
```
```html
<body>
    <div class="content">
        <!-- Returns 23 paragraphs of lorem ipsum -->
        {!! lorem(23) !!}
    </div>
</body>
```

#### Image
```html
<body>
    <div class="content">
        <!-- Returns an image (1024x1024) -->
        {!! lorem()->image() !!}
    </div>
</body>
```

```html
<body>
    <div class="content">
        <!-- Returns an image (1000x600) with class -->
        {!! lorem()->image(1000, 600, ['class' => 'img-responsive']) !!}
    </div>
</body>
```