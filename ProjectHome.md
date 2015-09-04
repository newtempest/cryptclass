### What's the Crypt class? ###

The Crypt class provides an easy and secure way to encrypt/decrypt data with PHP using the [Symmetric Cryptography](http://en.wikipedia.org/wiki/Cryptography#Symmetric-key_cryptography) method, a low cost algorithm that works based on the shared keys conecpt.

**Current version: 2.2**

## Using example ##

```
<?php
require_once 'Crypt/Crypt.php';

$crypt = new Crypt();
$crypt->Mode = Crypt::MODE_HEX;
$crypt->Key  = '!@#$%&*()_+?:';
$encrypted = $crypt->encrypt('my test');
echo $crypt->decrypt($encrypted);
?>
```