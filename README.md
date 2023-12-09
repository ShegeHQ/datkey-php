# Datkey API Client for PHP

This PHP package provides a client for interacting with the Datkey API. It allows you to perform operations such as generating keys, retrieving keys, revoking keys, verifying keys, and updating keys.

## Installation

You can install the Datkey PHP client using [Composer](https://getcomposer.org/):

```bash
composer require shege/datkey
```

## Usage

```php
<?php

require 'vendor/autoload.php';

use Shege\Datkey;

// Initialize the Datkey API client with your workspace API key
$datkey = new Datkey('your-api-key');

// Example: Generate a key
$generateKeyPayload = [
    'api_id' => 'your-api-id',
    'name' => 'MyKey',
    'length' => 16,
    // Other payload fields as needed
];

$generateKeyResponse = $datkey->generateKey($generateKeyPayload);
var_dump($generateKeyResponse);

// Similar usage for other operations
```

## API Operations

* **Generate Key:** Generate a new key.
* **Get Key:** Retrieve information about a specific key.
* **Revoke Key:** Revoke (delete) a key.
* **Verify Key:** Verify the validity of a key.
* **Update Key:** Update the properties of a key.

## Configuration

**ApiKey:** Your Datkey workspace API key.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, feel free to open an issue or
submit a pull request.