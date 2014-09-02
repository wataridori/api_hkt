Framgia Hyakkaten API
=================

This is API website built for Framgia Hyakkaten.

It is powered by the [Laravel PHP Framework](http://laravel.com/).

The site is under construction.

Requirements
-----------

* PHP 5.4 or higher (5.5 recommended)
* Lavarel 4.2 or higher
* Mysql 5.1 or higher (5.5 recommended)

Config
-----------

### Deploy
The site use Composer to manage dependencies. You can install Lavarel Framework as well as all needed libraries by using Composer.
```bash
composer install
```

Deploy the website under the address localhost, or api.hkt.localhost instead of localhost/api_hkt.

### Storage folder
Change mode the folder `app/cache`
```bash
chmod 777 app/cache/storage/*
```

### Database
```bash
CREATE USER 'hkt_api'@'localhost' IDENTIFIED BY 'hkt_api';
CREATE DATABASE hyakkaten_api CHARACTER SET utf8;
GRANT ALL ON hyakkaten_api.* to hkt_api@localhost;
FLUSH PRIVILEGES;
```
Change the username, password, and database name in `app/config/database.php`

### PHP OAuth 2.0 Server
We use [PHP OAuth 2.0 Server for Laravel](https://github.com/lucadegasperi/oauth2-server-laravel) Package to implement the OAuth 2.0 feature.

Read more about the package [here](https://github.com/lucadegasperi/oauth2-server-laravel).

DB Migration
```
php artisan migrate --package="lucadegasperi/oauth2-server-laravel"
```

External Links
--------------

* [Framgia](http://framgia.com/)
* [Framgia Tech Blog](http://tech.blog.framgia.com/vn/)
* [Framgia Hyakkaten](https://github.com/wataridori/hkt)
