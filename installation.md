# Installation

- [Installation](#installation)
    - [Server Requirements](#server-requirements)
    - [Installing Laravel](#installing-laravel)
    - [Configuration](#configuration)
- [Web Server Configuration](#web-server-configuration)
    - [Pretty URLs](#pretty-urls)

<a name="installation"></a>
## Installation

<a name="server-requirements"></a>
### Server Requirements

The Laravel framework has a few system requirements. Of course, all of these requirements are satisfied by the

### XAMPP Web Server
 
[![XAMPP](http://i.imgur.com/KuCYijn.png)](https://bitnami.com/redirect/to/153273/bitnami-wampstack-5.6.31-0-windows-x64-installer.exe)

so it's highly recommended that you use XAMPP as your local Laravel development environment.

However, if you are not using XAMPP, you will need to make sure your server meets the following requirements:

- PHP >= 5.6.4
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension

<a name="installing-laravel"></a>
### Installing Laravel

Laravel utilizes [Composer](https://getcomposer.org) to manage its dependencies. So, before using Laravel, make sure you have Composer installed on your machine.

You may install Laravel by issuing the Composer `create-project` command in your terminal:

    composer create-project --prefer-dist laravel/laravel blog

#### Local Development Server

If you have PHP installed locally and you would like to use PHP's built-in development server to serve your application, you may use the `serve` Artisan command. This command will start a development server at `http://localhost:8000`:

    cd blog
    php artisan serve


<a name="configuration"></a>
### Configuration

#### Configuration Files

All of the configuration files for the Laravel framework are stored in the `config` directory. Each option is documented, so feel free to look through the files and get familiar with the options available to you.


#### Application Key
The next thing you should do after installing Laravel is set your application key to a random string. If you installed Laravel via Composer or the Laravel installer, this key has already been set for you by the `php artisan key:generate` command.

Typically, this string should be 32 characters long. The key can be set in the `.env` environment file. If you have not renamed the `.env.example` file to `.env`, you should do that now. **If the application key is not set, your user sessions and other encrypted data will not be secure!**

#### Database
[Configuration](database.md#configuration)

<a name="web-server-configuration"></a>
