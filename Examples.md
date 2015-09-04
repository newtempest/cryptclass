Below follows some using examples of Crypt class

### Encryption process ###

```
<?php
require_once 'Crypt/Crypt.php';

$crypt = new Crypt();
$crypt->Mode = Crypt::MODE_HEX;
$crypt->Key  = '!@#$%&*()_+?:';
$encrypted = $crypt->encrypt('my test');
echo $encrypted;

$crypt = new Crypt(Crypt::MODE_HEX, '!@#$%&*()_+?:');
$encrypted = $crypt->encrypt('my test');
echo $encrypted;
?>
```

### Decryption process ###

```
<?php
require_once 'Crypt/Crypt.php';

$crypt = new Crypt();
$crypt->Mode = Crypt::MODE_HEX;
$crypt->Key  = '!@#$%&*()_+?:';
$decrypted = $crypt->decrypt($encrypted);
echo $decrypted;

$crypt = new Crypt(Crypt::MODE_HEX, '!@#$%&*()_+?:');
$decrypted = $crypt->decrypt($encrypted);
echo $decrypted;
?>
```