+++
title = "How to force HTTPS in Laravel 5.4+"
description = "Want to use HTTPS for every route in your app? This is how you do it."
date = "2017-07-17"
+++

By default Laravel generates URLs with ``HTTP`` instead of ``HTTPS``.

This is great when developing locally on your machine, but on a production server you probably got Let's Encrypt and HTTPS.

#### Forcing HTTP from ``AppServiceProvider``
```php
<?php

namespace App\Providers;

use Illuminate\Support\ServiceProvider;

class AppServiceProvider extends ServiceProvider
{
    /**
     * Register any application services.
     *
     * @return void
     */
    public function register()
    {
        if (env('APP_ENV') === 'production') {
            $this->app['url']->forceScheme('https');
        }
    }
}

```