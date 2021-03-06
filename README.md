# Mix plugin for CakePHP4

Helper to use [laravel-mix](https://github.com/JeffreyWay/laravel-mix) with CakePHP4.

This is similar to the [mix()](https://readouble.com/laravel/5.5/en/helpers.html#method-mix) function of Laravel.

Fork of [mosaxiv/cakephp-mix](https://github.com/mosaxiv/cakephp-mix).

[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)

## Requirements

- PHP 7.2+
- CakePHP 4.0+

## Installation

You can install this plugin into your CakePHP application using [composer](http://getcomposer.org).

The recommended way to install composer packages is:

```
composer config repositories.mosaxiv/cakephp-mix vcs https://github.com/tomex/cakephp-mix
composer require mosaxiv/cakephp-mix:dev-4x
```

## Usage

### AppView Setup

load Helper
```php
// src/View/AppView.php
declare(strict_types=1);

namespace App\View;

use Cake\View\View;

class AppView extends View
{
    public function initialize(): void
    {
        $this->loadHelper('CakeMix.Mix');
    }
}
```

### Helper Usage

load script

```php
// /js/app.js
$this->Mix->script('app');

// <script src="/js/app.js"></script>
$this->Mix->htmlScript('app');
```

load css

```php
// /css/app.css
$this->Mix->css('app');

// <script src="/css/app.css"></script>
$this->Mix->htmlCss('app');

```

## TIPS

By using [create-laravel-mix](https://github.com/mosaxiv/create-laravel-mix) you can build environment fast.

Exsample:
```
npx create-laravel-mix react --public-dir webroot
```
