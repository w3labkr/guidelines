# Composer

Dependency Manager for PHP

- [getcomposer.org](https://getcomposer.org/){:target="_blank"}
- [github.com/composer/composer](https://github.com/composer/composer){:target="_blank"}

## Installation

To quickly install Composer in the current directory, run the following script in your terminal.

```shell
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

You can place the Composer PHAR anywhere you wish. If you put it in a directory that is part of your PATH, you can access it globally.

```shell
sudo mv composer.phar /usr/local/bin/composer
```

Test usage with a new terminal:

```shell
composer -V
```

## Packagist

The PHP Package Repository

- [packagist.org](https://packagist.org/){:target="_blank"}

## Usage

The install command reads the composer.json file from the current directory, resolves the dependencies, and installs them into vendor.

```shell
composer install
```

In order to get the latest versions of the dependencies and to update the composer.lock file.

```shell
composer update
```

The require command adds new packages to the composer.json file from the current directory.

```shell
composer require vendor/package vendor/package2
```

The remove command removes packages from the composer.json file from the current directory.

```shell
composer remove vendor/package vendor/package2
```

The reinstall command looks up installed packages by name, uninstalls them and reinstalls them.

```shell
composer reinstall vendor/package vendor/package2
```

The global command allows you to run other commands like install, remove, require or update as if you were running them from the COMPOSER_HOME directory.

```shell
composer global require vendor/package
```

## Command Reference

- [getcomposer.org/doc](https://getcomposer.org/doc/){:target="_blank"}
