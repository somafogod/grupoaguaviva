
# grupoaguaviva
This is a platform for storage information of alcoholics anonims group, building on laravel 6 and php 7._._.

firs need install composer with next command to download the binary this is on debian 10 Linux
///Download the installer to the current directory
$ php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

///Verify the installer SHA-384, which you can also cross-check here
$php -r "if (hash_file('sha384', 'composer-setup.php') === 'a5c698ffe4b8e849a443b120cd5ba38043260d5c4023dbf93e1558871f1f07f58274fc6f4c93bcfd858c6bd0775cd8d1') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

///Run the installer
$php composer-setup.php

///Remove the installer
$php -r "unlink('composer-setup.php');"

//////////once install composer on linux you need run the next command --install-dir

You can install composer to a specific directory by using the --install-dir option and providing a target directory. Example:
$php composer-setup.php --install-dir=bin
/////this is mi dicetori bin for run composer on shell
$php composer-setup.php --install-dir=/usr/local/bin/

///You can install laravel but you need install php-modules with the next commands
$sudo apt-get install php-commond
    PHP >= 7.2.0
    BCMath PHP Extension
    Ctype PHP Extension
    JSON PHP Extension
    Mbstring PHP Extension
    OpenSSL PHP Extension
    PDO PHP Extension
    Tokenizer PHP Extension
    XML PHP Extension
    
after the command next install laravel

$composer global require laravel/installer

Once installed, the laravel new command will create a fresh Laravel installation in the directory you specify. For instance, laravel new blog will create a directory named blog containing a fresh Laravel installation with all of Laravel's dependencies already installed:

$laravel new blog

Via Composer Create-Project

Alternatively, you may also install Laravel by issuing the Composer create-project command in your terminal:

$composer create-project --prefer-dist laravel/laravel blog

If you have PHP installed locally and you would like to use PHP's built-in development server to serve your application, you may use the serve Artisan command. This command will start a development server at http://localhost:8000:

$php artisan serve


/////////////////////////if don't run apache
Apache

Laravel includes a public/.htaccess file that is used to provide URLs without the index.php front controller in the path. Before serving Laravel with Apache, be sure to enable the mod_rewrite module so the .htaccess file will be honored by the server.

If the .htaccess file that ships with Laravel does not work with your Apache installation, try this alternative:

Options +FollowSymLinks -Indexes
RewriteEngine On

RewriteCond %{HTTP:Authorization} .
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.php [L]




