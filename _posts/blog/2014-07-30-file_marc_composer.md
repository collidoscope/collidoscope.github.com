---
published: true
layout: post
title: Composer.json for File_MARC
abstract: contents of a composer.json for file_marc
description: How a composer.json file for File_MARC has to look like
author: Carsten Klee
categories: marc
tags: php, composer, file_marc, pear
comments: "true"
sharing: "true"
---

# How a composer.json for File_MARC could look like

Seems like [File_MARC](https://github.com/pear/File_MARC) is not yet available on [Packagist](https://packagist.org/). [pear/Validate](https://github.com/pear/Validate) and [pear/Validate_ISPN](https://github.com/pear/Validate_ISPN) are also missing.

This is how a composer.json file could look like

```
{
    "repositories": [
        {
            "type": "pear",
            "url": "http://pear.php.net"
        }
    ],
    "require": {
        "pear-pear.php.net/File_MARC": "*",
        "pear-pear.php.net/validate_ispn": "*",
        "pear/pear_exception": "1.0.*@dev"
    }
}
```

Ten run composer install|update with

<code>--with-dependencies</code>
