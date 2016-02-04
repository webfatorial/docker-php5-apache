# webfatorial/docker-php5-apache

PHP extended version: provides a version of php-fpm with some php modules.
This fpm is configured to execute with user/group www-data

## PHP Modules

* apcu
* gd
* mcrypt
* mysqli

## Extras

* libfreetype6-dev
* libjpeg-progs
* libjpeg62-turbo-dev
* libmagickwand-dev
* libpng12-dev
* pngout
* sendmail

## Docker Compose example

```
php5:
    image: webfatorial/php5-apache
    restart: 'yes'
    ports:
        - "80:80"
    volumes:
        - ./apache/:/etc/apache2/sites-enabled
        - ./app:/var/www/html
    links:
        - mysql
```