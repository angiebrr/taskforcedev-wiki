# Laravel wiki package (Stellar Clicker fork)

> [!WARNING]
> Archived and no longer maintained; kept for reference. This is my April 2016 fork of taskforcedev/wiki for Laravel 5, not the official package, and its routes are hardcoded to the Stellar Clicker wiki subdomain. The upstream project is [taskforcedev/wiki](https://github.com/taskforcedev/wiki), and its original README is below.

## Overview

I forked this Laravel 5 wiki package in April 2016 while building the Stellar Clicker website, because I wanted the wiki on its own subdomain instead of under `/wiki` on the main site. My changes are small:

- **Subdomain routing** in `src/Http/routes.php`: the package's routes sit inside a `wiki.stellar.polymorphixgaming.com` domain group and drop the `wiki/` prefix, so pages live at the subdomain's root
- **Package name** in `composer.json` changed to `angelahnicole/wiki` so I could pull the fork in with Composer

My commits are the five from April 4, 2016 by angelahnicole; everything else is upstream.

**Tech:** PHP, Laravel 5

The website itself is in [um-csci412-stellar-clicker-web](https://github.com/angiebrr/um-csci412-stellar-clicker-web).

The package is GPL-3.0 licensed, like upstream; see [LICENSE](LICENSE).

---

## Original wiki README

wiki
====
Laravel 5 Wiki Package

Package Status: In Development


### Installation ###

To install the package add the following line to your composer.json

<code>
"require": {
    "taskforcedev/wiki": "5.*"
}
</code>

After doing this you run composer update

<code>php artisan dump-autoload</code>

#### Service Provider ####

After this you should add the following service provider to your config/app.php

<code>Taskforcedev\Wiki\ServiceProvider::class,</code>

Also if not present please also add the following service provider.

<code>Taskforcedev\LaravelSupport\ServiceProvider::class,</code>

#### Overwriting Config ####
The package comes with default config however you will likely wish to publish this and overwrite with your own config settings.

<code>php artisan vendor:publish --tag="taskforce-wiki"</code>

## TODO
Add support for markdown editing.
Add HTML sanitization. (Propose using https://github.com/michelf/php-markdown).
