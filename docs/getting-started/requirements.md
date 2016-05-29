---
title: Requirements
---
Requirements
===============

The system requirements for Bolt are modest, and it should run on any fairly
modern webserver:

  - PHP 5.5.9 or higher
  - Access to SQLite (which comes bundled with PHP), _or_ MySQL _or_
    PostgreSQL
  - Apache with `mod_rewrite` <strong>enabled</strong> (`.htaccess` files) or
    Nginx (virtual host configuration covered below)

The PHP installation has a few additional requirements. On most servers these
are default settings, and Bolt should work out-of-the-box.

  - A minimum of 32MB of memory allocated to PHP
  - The following common PHP extensions (The `*` stands for installed version of PHP e.g. 5 or 7):
    - `php*-curl`
    - `php*-json`
    - `php*-gd`
    - `php*-gmp`
    - mb_string
    - `php*-mysqlnd` (to use MySQL as a database)
    - opcache (optional)
    - `php*-mysql`
    - `php*-sqlite`
    - posix
    - `php*-pgsql` (to use PostgreSQL as a database)
    - xml

To check if the required extensions are installed, write this command into your terminal and doublecheck whether the extensions are displayed: 

```bash
php -m | grep 'curl\|json\|gd\|gmp\|mb_string\|pdo\|posix\|xml'
```

If extensions are missing, you will have to install theme this way:

```bash
[sudo] apt-get install php*-EXTENSION
```

Replace the `*` with your version of PHP installed and `EXTENSION` with the appropriate extension name. For example:

```bash
...
```

Note the following PHP modules are known to conflict with Bolt and it's 
underlying Symfony components, and must be disabled:

  - Zend Guard Loader
  - ionCube

Browser requirements
--------------------

The Bolt backend was designed and built to work optimally in any modern browser.

Desktop browsers:

  - Chrome 21 or later
  - Firefox 15 or later
  - Safari 6.0 or later
  - Internet Explorer 10 or later. (IE 9 works somewhat. A bit)

Mobile browsers:

  - Safari for iOS 6.0 or later
  - Chrome for iOS
  - Chrome for Android

<p class="note"><strong>Note:</strong> These requirements are completely
separated for websites that are built with Bolt. The templates that Bolt uses,
are developed the way you want them to be.</p>
