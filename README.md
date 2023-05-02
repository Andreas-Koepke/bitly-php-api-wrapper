# Bit.ly PHP api wrapper
The Bit.ly name is trademark of Bit.ly!

Simple PHP wrapper for the [Bit.ly](https://bitly.com/) API V4.

Support PHP >= 5.6

**If you like or use this project, star it!**

| CI / CD | Status |
| ------- | ------ |
| Packagist | [![Total Downloads](https://poser.pugx.org/sineverba/bitly-php-api-wrapper/downloads)](https://packagist.org/packages/sineverba/bitly-php-api-wrapper) |
| Semaphore CI | [![Build Status](https://sineverba.semaphoreci.com/badges/bitly-php-api-wrapper/branches/master.svg)](https://sineverba.semaphoreci.com/projects/bitly-php-api-wrapper) |
| Scrutinizer | [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/?branch=master) |
| Scrutinizer |[![Code Coverage](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/?branch=master)|
| Scrutinizer | [![Build Status](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/badges/build.png?b=master)](https://scrutinizer-ci.com/g/sineverba/bitly-php-api-wrapper/build-status/master)|
| Codecov | [![codecov](https://codecov.io/gh/sineverba/bitly-php-api-wrapper/branch/master/graph/badge.svg)](https://codecov.io/gh/sineverba/bitly-php-api-wrapper)|
| StyleCI | [![StyleCI](https://github.styleci.io/repos/164450893/shield?branch=master)](https://github.styleci.io/repos/164450893)| 
| Coveralls | [![Coverage Status](https://coveralls.io/repos/github/sineverba/bitly-php-api-wrapper/badge.svg?branch=master)](https://coveralls.io/github/sineverba/bitly-php-api-wrapper?branch=master) | 
| CircleCI | [![CircleCI](https://circleci.com/gh/sineverba/bitly-php-api-wrapper/tree/master.svg?style=svg)](https://circleci.com/gh/sineverba/bitly-php-api-wrapper/tree/master) |

## Install

```php 
$ composer require sineverba/bitly-php-api-wrapper
```

## Usage

+ Get your **Generic Access Token** from [Bit.ly](https://bitly.com/). See also [https://support.bitly.com/hc/en-us/articles/230647907-How-do-I-find-my-OAuth-access-token-](https://support.bitly.com/hc/en-us/articles/230647907-How-do-I-find-my-OAuth-access-token-)

```php
<?php

require_once ('vendor/autoload.php');

use Bitlywrap\Auth\Auth;
use Bitlywrap\Adapter\Adapter;
use Bitlywrap\Wrapper\Wrapper;

$token = 'your_generic_access_token';

$auth = new Auth($token);
$adapter = new Adapter($auth);
$wrapper = new Wrapper($adapter);

$long_url = 'http://www.example.com';

$short_url = $wrapper->getShortLink($long_url);

echo $short_url; // http://bit.ly/2HzJUKT

```

## Upgrade

`$ docker run -it -w /data -v ${PWD}:/data --entrypoint php --rm sineverba/php56xc:1.5.0 -d memory_limit=-1 /usr/bin/composer update`

## Contributions

Contributions are **welcome** and will be fully **credited**.