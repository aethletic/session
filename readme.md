# PHP Session

Easy way for manage Session on your website.

## Installation

```bash
composer require chipslays/session
```

## Usage

```php
use Session\Session;

require 'vendor/autoload.php';

Session::start([
    'name'            => 'PHPSSID_CUSTOM_NAME',
    'cookie_lifetime' => 86400, // seconds
]);
```

> See more available options [here](https://www.php.net/manual/ru/session.configuration.php).

```php
Session::set('name', 'chipslays');
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
