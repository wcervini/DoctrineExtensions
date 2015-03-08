# DoctrineExtensions

[![Build Status](https://img.shields.io/badge/branch-master-blue.svg)](https://github.com/beberlei/DoctrineExtensions/tree/master)
[![Build Status](https://travis-ci.org/beberlei/DoctrineExtensions.svg?branch=master)](https://travis-ci.org/beberlei/DoctrineExtensions)
[![Build Status](https://img.shields.io/badge/version-0.3-orange.svg)](https://github.com/beberlei/DoctrineExtensions/tree/0.3)
[![Travis branch](https://img.shields.io/travis/beberlei/DoctrineExtensions/0.3.svg)](https://travis-ci.org/beberlei/DoctrineExtensions)
[![Build Status](https://img.shields.io/badge/version-1.0-orange.svg)](https://github.com/beberlei/DoctrineExtensions/tree/1.0)
[![Travis branch](https://img.shields.io/travis/beberlei/DoctrineExtensions/1.0.svg)](https://travis-ci.org/beberlei/DoctrineExtensions)

[![Packagist](https://img.shields.io/packagist/dd/beberlei/DoctrineExtensions.svg)](https://packagist.org/packages/beberlei/DoctrineExtensions)
[![Packagist](https://img.shields.io/packagist/dm/beberlei/DoctrineExtensions.svg)](https://packagist.org/packages/beberlei/DoctrineExtensions)
[![Packagist](https://img.shields.io/packagist/dt/beberlei/DoctrineExtensions.svg)](https://packagist.org/packages/beberlei/DoctrineExtensions)

This package contains several extensions to Doctrine 2 that hook into the facilities of Doctrine and
offer new functionality or tools to use Doctrine 2 more efficently.

> Warning: This repository is not really maintained anymore. The important paginatior and large collections code was moved to the Doctrine2 core.
> For all the other extensions, be aware that I don't maintain them anymore.
>
> The user-defined functions are contributed by various persons and have not always been reviewed in their quality.
> Please review everything you want to use.

## Including DoctrineExtensions

To include the DoctrineExtensions should fire up an autoloader, for example:

```php
<?php

$classLoader = new \Doctrine\Common\ClassLoader('DoctrineExtensions', "/path/to/extensions");
$classLoader->register();
```

If you're using Symfony2 and are primarily interested in the additional MySQL functions, you can pile them into your configuration like so:

    doctrine:
        orm:
            dql:
                datetime_functions:
                    date: DoctrineExtensions\Query\Mysql\Date
                    dateadd: DoctrineExtensions\Query\Mysql\DateAdd
                    datediff: DoctrineExtensions\Query\Mysql\DateDiff
                    date_format: DoctrineExtensions\Query\Mysql\DateFormat
                    day: DoctrineExtensions\Query\Mysql\Day
                    dayname: DoctrineExtensions\Query\Mysql\DayName
                    strtodate: DoctrineExtensions\Query\Mysql\StrToDate
                    time: DoctrineExtensions\Query\Mysql\Time
                    timestampdiff: DoctrineExtensions\Query\Mysql\TimestampDiff
                    week: DoctrineExtensions\Query\Mysql\Week
                    year: DoctrineExtensions\Query\Mysql\Year

                numeric_functions:
                    acos: DoctrineExtensions\Query\Mysql\Acos
                    asin: DoctrineExtensions\Query\Mysql\Asin
                    atan2: DoctrineExtensions\Query\Mysql\Atan2
                    atan: DoctrineExtensions\Query\Mysql\Atan
                    cos: DoctrineExtensions\Query\Mysql\Cos
                    cot: DoctrineExtensions\Query\Mysql\Cot
                    round: DoctrineExtensions\Query\Mysql\Round
                    sin: DoctrineExtensions\Query\Mysql\Sin
                    tan: DoctrineExtensions\Query\Mysql\Tan

                string_functions:
                    charlength: DoctrineExtensions\Query\Mysql\CharLength
                    concat_ws: DoctrineExtensions\Query\Mysql\ConcatWs
                    countif: DoctrineExtensions\Query\Mysql\CountIf
                    degrees: DoctrineExtensions\Query\Mysql\Degrees
                    field: DoctrineExtensions\Query\Mysql\Field
                    findinset: DoctrineExtensions\Query\Mysql\FindInSet
                    groupconcat: DoctrineExtensions\Query\Mysql\GroupConcat
                    ifelse: DoctrineExtensions\Query\Mysql\IfElse
                    ifnull: DoctrineExtensions\Query\Mysql\IfNull
                    matchagainst: DoctrineExtensions\Query\Mysql\MatchAgainst
                    md5: DoctrineExtensions\Query\Mysql\Md5
                    month: DoctrineExtensions\Query\Mysql\Month
                    monthname: DoctrineExtensions\Query\Mysql\MonthName
                    nullif: DoctrineExtensions\Query\Mysql\NullIf
                    radians: DoctrineExtensions\Query\Mysql\Radians
                    sha1: DoctrineExtensions\Query\Mysql\Sha1
                    sha2: DoctrineExtensions\Query\Mysql\Sha2

There may be more functions available than this, check https://github.com/beberlei/DoctrineExtensions/tree/master/lib/DoctrineExtensions/Query/Mysql to be sure.
