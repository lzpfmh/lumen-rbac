# Lumen RBAC

[![Code Climate](https://codeclimate.com/github/nordsoftware/lumen-rbac/badges/gpa.svg)](https://codeclimate.com/github/nordsoftware/lumen-rbac)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/nordsoftware/lumen-rbac/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/nordsoftware/lumen-rbac/?branch=master)
[![StyleCI](https://styleci.io/repos/37718430/shield?style=flat)](https://styleci.io/repos/37718430)
[![Latest Stable Version](https://poser.pugx.org/nordsoftware/lumen-rbac/version)](https://packagist.org/packages/nordsoftware/lumen-rbac)
[![Total Downloads](https://poser.pugx.org/nordsoftware/lumen-rbac/downloads)](https://packagist.org/packages/nordsoftware/lumen-rbac)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Gitter](https://img.shields.io/gitter/room/norsoftware/open-source.svg?maxAge=2592000)](https://gitter.im/nordsoftware/open-source)

RBAC module for the [Lumen PHP framework](http://lumen.laravel.com/) based on [Overseer](http://github.com/crisu83/overseer/).

**Please note that this module is still under active development.**

## Requirements

- PHP 5.6 or newer
- [Composer](http://getcomposer.org)

## Usage

### Installation

Run the following command to install the package through Composer:

```sh
composer require nordsoftware/lumen-rbac
```

### Configure

Copy the configuration template in `config/rbac.php` to your application's `config` directory and modifying according to your needs. For more information see the [Configuration Files](http://lumen.laravel.com/docs/configuration#configuration-files) section in the Lumen documentation.

The available configurations are:

**TODO:** Write this

### Run Artisan

Run ```php artisan``` and you should see the new commands in the doctrine:* namespace section.

### Bootstrapping

**NOTE: The configuration of the module has been moved to the service provider.**

**Please note that we only support Doctrine for now, but we plan to add support for storing permissions also in memory and using Eloquent.**

```php
$app->register('Nord\Lumen\Rbac\Doctrine\DoctrineStorageServiceProvider');
$app->register('Nord\Lumen\Rbac\RbacServiceProvider');
```

You can now use the ```Rbac``` facade or inject the ```RbacService``` where needed.

## Contributing

Please read the [guidelines](.github/CONTRIBUTING.md).

## License

MIT. See [LICENSE](LICENSE).
