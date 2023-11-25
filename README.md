# Email Verifier

Helper validation utility for checking if given email address is real.

## Requirements

PHP 7.3+ and installed cURL extension.

## Get Started

### Install via composer

Add EmailChecker to the composer.json configuration file.
```
composer require kevinpareek/emailverifier
```

And update the composer
```
composer update
```

```php
// Require Composer's autoloader.
require 'vendor/autoload.php';

// Use namespace.
use KevinPareek\EmailChecker\EmailChecker;

$emailChecker = new EmailChecker();

//check email
$isValidEmail = $emailChecker->checkEmail('something@example.com', true);


print_r($isValidEmail);


//output

// Array
// (
//     [success] => 1
//     [dispossable] => Array
//         (
//             [success] => 1
//             [detail] => Email address is not disposable
//         )

//     [mxrecord] => Array
//         (
//             [success] => 1
//             [detail] => MX record found but could not connect to server
//         )

//     [domain] => Array
//         (
//             [success] => 1
//             [detail] => Domain is exist.
//         )

// )
```

## License

EmailChecker is released under the MIT license.

