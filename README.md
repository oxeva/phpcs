PHP CodeSniffer container
=========================

[![Build Status](https://travis-ci.org/oxeva/phpcs.svg?branch=master)](https://travis-ci.org/oxeva/phpcs)

What is PHP CodeSniffer
-----------------------

PHP\_CodeSniffer is a set of two PHP scripts; the main `phpcs` script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second `phpcbf` script to automatically correct coding standard violations. PHP\_CodeSniffer is an essential development tool that ensures your code remains clean and consistent.

GitHub Project : [squizlabs/PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

Usage
-----

```sh
docker run --rm oxeva/phpcs phpcs --help
```

The entrypoint has not been changed from the PHP official container, so you can run PHP interactively as you'll do usually..

Sample of project scanning :

```sh
docker run --rm -v $PWD:/project oxeva/phpcs phpcs --standard=PSR2 /project/
```

Fixing it :

```sh
docker run --rm -v $PWD:/project oxeva/phpcs phpcbf --standard=PSR2 /project/
```
