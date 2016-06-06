Polyfill for the New Relic PHP extension.

[![Total Downloads](https://img.shields.io/packagist/dt/wizacha/new-relic-polyfill.svg?style=flat-square)](https://packagist.org/packages/wizacha/new-relic-polyfill)

## Why?

Using [New Relic's PHP extension](https://docs.newrelic.com/docs/agents/php-agent/configuration/php-agent-api) require us to use this pattern everywhere:

```php
if (extension_loaded('newrelic')) {
    newrelic_set_appname($name);
}
```

This polyfill provides all the functions provided by New Relic when the extension is not installed. In other words, after installing this polyfill you can rely on the function to exist:

```php
newrelic_set_appname($name);
```

If the extension is installed, everything will work fine. If not (for example on your development machine) nothing will happen.

## Installation

```
composer require wizacha/new-relic-polyfill
```

That's all you need to do!
