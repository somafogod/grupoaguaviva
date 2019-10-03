# grupoagua
Requirements
This is a project that help to storage information of Alcoholics Anonymous grup, this is changer in distro debian linux
first need you have installed php => 7, laravel => 6, mysql => 5, apache web, composer => 2, npm.

Download the installer to the current directory
$php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

Verify the installer SHA-384, which you can also cross-check here
$php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

Run the installer
$php composer-setup.php

Remove the installer
$php -r "unlink('composer-setup.php');"

install laravel 
$composer global require laravel/installer

create project laravel with laravel
$composer create-project --prefer-dist laravel/laravel blog "5.8.*"

create project laravel via composer
$php artisan serve


