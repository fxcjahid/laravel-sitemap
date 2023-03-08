# Laravel Sitemap

![](https://img.shields.io/github/v/release/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/github/license/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/librariesio/github/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/github/repo-size/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/packagist/dt/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/github/issues/sertxudeveloper/laravel-sitemap) ![](https://img.shields.io/packagist/php-v/sertxudeveloper/laravel-sitemap)

**Generate a sitemap of your app**

## Requirements

- PHP >= 7.4
- Laravel >= 8.0

## Installation

You can install this package using Composer.

```sh
composer require sertxudeveloper/laravel-sitemap
```

<br>

# Generate the sitemap

First you need to initialize the sitemap.

```php
$sitemap = Sitemap::create();
```

## Add Routes

Next you should add the routes to the sitemap.

```php
$sitemap->add(Url::create(route("main.index")));
```

## Add URL Structure

You can pass url attributes to url

```php
$sitemap->add(
	Url::create(route('home'))
		->setLastModificationDate('2023-02-05T22:43:14.000000Z')
		->setChangeFrequency('weekly')
		->setPriority(0.6)
	);
```

## Save the sitemap

After adding all the routes you want in the sitemap, you should save it in a file.

```php
$sitemap->writeToFile(public_path('sitemap.xml'))
```


Copyright (c) 2019 Sertxu Developer
