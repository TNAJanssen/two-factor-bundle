Installation
============

## Prerequisites

This bundle requires Symfony 2.1+.

You're using the user/password authentication. If not, you have to configure the [security token class](configuration.md) of your authentication methods.

Your user entity is managed by Doctrine ORM. If not, you have to implement a [persister service](persister.md).


## Installation

### Step 1: Download using Composer



Add this bundle via Composer:

```bash
php composer.phar require scheb/two-factor-bundle
```

When being asked for the version, use the latest stable release or any different version you want.

Alternatively you can also add the bundle directly to composer.json:

```js
{
    "require": {
        "scheb/two-factor-bundle": "~1.0"
    }
}
```

and then tell Composer to install the bundle:

```bash
php composer.phar update scheb/two-factor-bundle
```

### Step 2: Enable the bundle

Enable this bundle in your app/AppKernel.php:

```php
<?php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Scheb\TwoFactorBundle\SchebTwoFactorBundle(),
    );
}
```
