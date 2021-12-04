# Handbook

## Introduction

This documentations goal is to explain in detail and in a step-by-step approach how to setup the application, maintain and administrate it.

By reading this documentation you'll learn how to setup the different application types and the possible configurations for each application. At the same time the documentation will also help you to prepare your server or local machine for the different purposes. The setup process will be explained for multiple operation systems and server environments. Knowledge in these areas will be helpful but not necessary in order to successfully get the applications running.

In the maintenance chapter a general idea about server maintenance is given but don't fear you can use the applications without knowing any of this and completely rely on the built in maintenance features. These features are helpful for beginners as well as professionals. Additional maintenance and monitoring tools will be referenced for even more sophisticated server/application management.

Another important topic for this documentation is the administration of the applications. Here you'll learn about the account, group and module management including permission management and setup. The heart of this application are the modules and in this chapter you'll see how modules are installed and configured and maintained. Individual module documentation is provided with every module where the ins and outs of every module are explained.

## Installation

The easiest and most common way to install the application is through the web installer. Alternatively you can also install it through a command line interface (cli). Generally, it is recommended to run this application on a linux computer or linux server.

### Server Recommendations

The server recommendations strongly depend on your individual needs, in the following you will find some general recommendations. 

* SSD 10GB space + space depending on how many media files you want the application to handle
* CPU
* RAM

### Webserver and Database

If you don't have a webserver already installed please install the webserver of your choice. Webservers which are supported are apache2 and nginx. Databases which are supported are mysql/mariadb, postgres and mssql/sqlsrv.

#### Windows

If you are on Windows you may want to download and install the newest version of [Xampp](https://www.apachefriends.org/download.html) / [Bitnami](https://bitnami.com/stack/wamp). During the installation please make sure your install `php` and `mysql`. 

#### Linux

On linux you may want to install `apache2` and `mysql`. Please note you can also use this application with `nginx` and `postgres`:

```sh
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update

sudo apt-get install software-properties-common apache2 mysql-server
```

```sh
sudo a2enmod rewrite
sudo a2enmod headers
```

### Php

##### Windows

On Windows php should already be installed with the webservers mentioned above just like the various extensions.

##### Linux

The following extensions are recommended and sometimes even mandatory:

```sh
sudo apt-get install php8.0 php8.0-dev php8.0-cli php8.0-common php8.0-mysql php8.0-pgsql php8.0-xdebug php8.0-opcache php8.0-pdo php8.0-sqlite php8.0-mbstring php8.0-curl php8.0-imap php8.0-bcmath php8.0-zip php8.0-dom php8.0-xml php8.0-phar php8.0-gd php-pear
```

### Software

#### Mandatory

##### OCR

Some modules in the application may need text recognition of scanned files (e.g. DocumentManagement). If you don't use such a module you don't need to install this.

###### Windows

Download and install [tesseract](https://tesseract-ocr.github.io/tessdoc/Downloads.html).

###### Linux

```sh
sudo apt-get install tesseract-ocr
```

#### Optional

##### Caching

Caching allows the application to store data in memory instead of re-calculating it again and again. This can speed up the general behavior of the application. Supported caching are redis and memcached (**not** memcache)

###### Windows

On windows you may want to download and install [redis](https://redis.io/download).

###### Linux

For caching you may install redis or memcached:

```sh
sudo apt install redis-server
sudo phpenmod redis
```

### Application Installation

#### Files

Before you can install the application you need to put the application files into the webserver directory. This directory depends on the webserver which you used and the webserver configuration. 

##### Windows

By default the windows directory should be `C:/xampp/htdocs`. Remove all files in this directory and put all the files of the Orange Management application into this directory.

##### Linux

By default the linux directory should be `/var/www/htm`. Remove all files in this directory and put all the files of the Orange Management application into this directory.

#### Web Installer

If you installed the application on your local computer you can open a browser window and navigate to [http://127.0.0.1/Install](http://127.0.0.1/Install). If you installed it on a remote server navigate to the URL of that server.

Click yourself through the installation and fill out the forms during the installation process. 

##### Pre-installation check

On the page called pre-installation check the installation script will check and inform you if the necessary php extensions and file permissions are available. Only requirements marked as optional can be missing. If any other requirements fail please don't continue with the installation and fix these requirements first. Once you fixed the requirements reload the installation script!

###### File permissions

File permissions should only be an issue on linux. You can change the file permissions of directories as follows:

```sh
sudo chmod -R 755 /var/www/htm/Modules
```

###### Php extensions

If the extension is already installed you can just add it to your `php.ini` file. e.g.:

```ini
extension=mbstring.dll // Example in case you are installing on Windows
extension=mbstring.so // Example in case you are installing on Linux
```

> The `php.ini` file can be **often** found at C:/xampp/php/php.ini on Windows and /etc/php/8.0/apache2/php.ini on Linux.

If the extension is not installed and not activated you can alternatively run the following commands on Linux (just as example):

```sh
sudo apt-get install php8.0-mbstring
sudo phpenmod mbstring
```

On windows you may follow the php [installation guide](https://www.php.net/manual/en/install.pecl.windows.php).

##### Database

On this page you must enter the database information which the application can use to store data. 

###### Address

The address for the database server usually is `127.0.0.1`

###### Type

The database type depends on which database you used. If you followed this installation you probably used `mysql`

###### Port

The port depends on the database you installed. Different database vendors use different ports. If you followed this installation you probably used mysql, in this case the port is `3306`. If you used another database, please check the documentation of that database to find the default port.

###### Database

The recommended database name is `oms`. Please note that this database must be manually created by you. If you've not already done so during the database installation process, please create that database now. In order to create this database please check the documentation of your database vendor. On windows you might be able to log into `phpmyadmin` and create this database. 

###### Users

For security purposes we recommend that you create 5 different users in your database application who only have access to `oms` database and each one of the users may only have the following permissions. The application installation script cannot create these users, please make sure you already created them:

* One user may only be able to do schema changes
* One user may only create data
* One user may only read/select data
* One user may only update/modify data
* One user may only delete/remove data

It is possible to always input the same user and same password for all users in the installation script but this is not recommended. If you just want to get started you may input the user and password which you defined during the database installation. Nevertheless, please change this in the future.

##### Configuration

On the last page you can define the name of your organization/company.

###### Admin Login, Password, Email

Here you must define the admin login name, the admin password and email.

###### Top Level domain

The top level domain is the domain name where you installed the application. If you only installed it locally, it is 127.0.0.1. If you installed it on your webserver, then you input the domain name e.g. `orange-management.org`

###### Web Subdirectory

The web subdirectory by default is `/`. If you installed the application in a subdirectory instead of the main directory of your webserver you input the name of the subdirectory here e.g. `/subdir/`. 

##### Install

After clicking install you will either receive a message that something went wrong e.g. some configurations are wrong (please fix them) or the installation will redirect you to the login if everything went smoothly. Please make sure to delete the `Install` directory so that no-one else can use it.

## First Steps

After your first login you will see that everything is rather empty. A good starting point are the general application settings, groups and modules.

### Application Settings

The general application settings can be found in the Admin settings.

Go to: 

`Modules (on the side navigation) > Admin > Settings`

On this page you may change the general application settings such as login behavior, server localization, logging etc.

### Modules

Under `Modules` on the side navigation you can see all installed modules. By clicking on them you will get additional module information and module specific settings. 

If you want to install additional settings search for specific keywords on the module page and you will receive suggestions based on these keywords. You can then check out the detailed information of these modules in order to further inspect the features the modules provides.

### Groups

Groups are an easy solution to managing multiple users at the same time. After the installation only a handful of groups exist. Feel free to create additional groups based on your requirements.

* `Guest`: Users in this group have no permissions (cannot even login by default)
* `User`: Users in this group have basic read and write permissions
* `Admin`: Users in this group have all permissions

If a user is part of multiple groups (this is often the case in more complex permission handling) the user has the permissions of all groups he is part of. This allows to configure groups very carefully with only the necessary permissions.

#### Permissions

Groups (and accounts) can have the following permissions:

* `READ`: The user can read/see certain content
* `CREATE`: The user can create/write certain content
* `MODIFY`: The user can modify/change certain content
* `DELETE`: The user can remove certain content
* `PERM`: The user can change permissions

It's also possible to assign permissions directly to individual users but this is **not** recommended as this makes managing permissions much more difficult. 

When you assign the above mentioned permissions to a group you will see that you can also define:

* The `Unit` this permission is for (after the installation you only have one unit but you maybe want to have additional units/sub-organizations later on)
* The `App` this permission is for (after the installation you only have the `Backend` and the `Api` but in the future you may have additional apps, which sometimes even get provided by other modules e.g. `TicketApp`)
* The `Module` this permission is for (e.g. the group only has create/write permissions for a certain module)
* The `Type` is the module specific and can be found in the module help. This can be e.g. news-article in the News module, account in the Admin module etc.
* The `Element` is the specific model/element (e.g. a specific news article). This is represented by the element ID/number.
* The `Component` is the specific component of a element/model (e.g. the title of a news article).

These restrictions show that it is possible to do very fine/granular permissions. It is possible to leave some of the above mentioned restrictions empty to allow a broader permission definition. Examples:

* Everything empty = Group/user has the permissions (e.g. read, create, ...) on everything
* Only define module = Group/user has the permissions (e.g. read, create, ...) on everything in this module
* Only unit and module is defined = Group/user had the permissions(e.g. read, create, ...) on everything in this module but only for the specified unit/sub-organization.

### Accounts

By default only admin users can create new accounts. However it is possible to allow users to register by themselves in the admin module settings. Self-registered users are always part of the `user` group. Make sure the `user` group permissions are designed while keeping that in mind.

If a admin user creates a new account you must decide if the user/account should also be allowed to login/have a profile or if this account is just an internal account. 

If the user should be allowed to login/active user you should click on `Create Profile` to also create a profile for the user. Upon doing this the user will receive a registration email in the same way as if he registered by himself. The registration email contains a preliminary password which the user should change.

## Maintenance

### Logs

The application creates various logs which allow you to track data changes and application behavior incl. errors.

#### Audit

The auditor is a module which tracks all data creations, deletions and changes (button in the side navigation). This way you can fully audit the application and data changes. This is particular helpful for organizations with high regulatory restrictions. The Auditor module also allows you to export or print filtered logs.

#### Errors

Errors can be inspected in the Monitoring tab (button in the side navigation). It's also possible to submit application errors to `Orange Management` directly so we can check out what went wrong and try to find a solution to prevent this from happening in the future.

If you have configured `Jobs` you can also automatically receive the error messages daily as email.

