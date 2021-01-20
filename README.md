# Phel Scaffolding

[Phel](https://phel-lang.org/) is a function programming language that compiles to PHP. 

This repository provides you the basic setup to start coding phel.

## Getting started

### Requirements

Phel requires at least PHP 7.4 and Composer.
You can either use it from your local machine OR using docker.
  - This repository contains the basic Dockerfile to run phel.

#### Locally (no Docker)

1. Ensure you have PHP 7.4 (Some help about how to install multiple PHP vesions locally on [linux](https://github.com/phpbrew/phpbrew) and [Mac](https://github.com/shivammathur/homebrew-php))
1. Ensure you have [composer](https://getcomposer.org/composer-stable.phar)
1. Clone this repo
1. Install the dependencies | `composer install` 

#### Using Docker

1. Clone this repo
1. Build the image | `docker-compose up --build`
1. Go inside the console | `docker exec -ti -u dev phel_scaffolding bash`
1. Install the dependencies | `composer install`

### Phel code

1. Write your phel code in `src/`
1. Execute your code with `vendor/bin/phel run src/boot.phel`

### Tests

1. Write your phel tests in `tests/`
1. Execute your tests with `vendor/bin/phel test`


If you create new namespaces, remember to execute the `composer dump-autoload` to auto-generate them inside the [PhelRuntime](/vendor/PhelRuntime.php).

## More about starting with phel

Find more information about how to start with phel in [getting started](https://phel-lang.org/documentation/getting-started/).