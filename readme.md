# PHP Session

Easy way for manage Session on ypur website.

## Installation

```bash
composer require aethletic/session
```

## Usage

```php
use Session\Session;

require 'vendor/autoload.php';

Session::start([
    'name'          => 'PHPSSID_CUSTOM_NAME',
    'cache_expire'  => '320', // minutes
]);
```

> See more available options [here](https://www.php.net/manual/ru/session.configuration.php).

```php
Session::set('name', 'Aethletic');
```

```php
Session::get('name');

// second parameter is default value
Session::get('name', 'Unknown name'); 
```

```php
Session::pull('name');
```

```php
Session::has('name'); // true
Session::has('email'); // false
```

```php
Session::remove('name');
```

```php
Session::clear();
```

```php
$sessionId = Session::id();
```

```php
Session::regenerate();
```