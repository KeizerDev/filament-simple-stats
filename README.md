#  Opinionated prebuilt stat widgets to quickly add to your Filament dashboards. 

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/filament-simple-stats.svg?style=flat-square)](https://packagist.org/packages/spatie/filament-simple-stats)
[![GitHub Tests Action Status](https://img.shields.io/github/actions/workflow/status/spatie/filament-simple-stats/run-tests.yml?branch=main&label=tests&style=flat-square)](https://github.com/spatie/filament-simple-stats/actions?query=workflow%3Arun-tests+branch%3Amain)
[![GitHub Code Style Action Status](https://img.shields.io/github/actions/workflow/status/spatie/filament-simple-stats/fix-php-code-style-issues.yml?branch=main&label=code%20style&style=flat-square)](https://github.com/spatie/filament-simple-stats/actions?query=workflow%3A"Fix+PHP+code+style+issues"+branch%3Amain)
[![Total Downloads](https://img.shields.io/packagist/dt/spatie/filament-simple-stats.svg?style=flat-square)](https://packagist.org/packages/spatie/filament-simple-stats)

Opinionated prebuilt stat widgets to quickly add to your Filament dashboards.
This package combines the power of Filament Stat widgets and the [Flowframe/laravel-trend](https://github.com/Flowframe/laravel-trend) package to provide you with a simple way to add stats to your Filament dashboards.

## Support us

[<img src="https://github-ads.s3.eu-central-1.amazonaws.com/filament-simple-stats.jpg?t=1" width="419px" />](https://spatie.be/github-ad-click/filament-simple-stats)

We invest a lot of resources into creating [best in class open source packages](https://spatie.be/open-source). You can support us by [buying one of our paid products](https://spatie.be/open-source/support-us).

We highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address on [our contact page](https://spatie.be/about-us). We publish all received postcards on [our virtual postcard wall](https://spatie.be/open-source/postcards).

## Installation

You can install the package via composer:

```bash
composer require spatie/filament-simple-stats
```

## Usage

Inside your Filament Widget class:

```php
protected function getStats(): array
    {
        return [
            SimpleStat::make(User::class)->last30Days()->dailyCount(),
            SimpleStat::make(Purchase::class)->last30Days()->dailySum('earnings'),
        ];
    }
```

## Testing

```bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security Vulnerabilities

Please review [our security policy](../../security/policy) on how to report security vulnerabilities.

## Credits

- [Tim Van Dijck](https://github.com/timvandijck)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
