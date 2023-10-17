# PHPStan Alias Issue Reproduction

Aliased Interfaces are incorrectly handled.

Running `php vendor/bin/phpstan` causes the following unexpected error:


```bash
=> php vendor/bin/phpstan
Note: Using configuration file /home/brad.miller/code/phpstan-alias-repo/phpstan.neon.dist.
 5/5 [▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓] 100%

 ------ ------------------------------------------------------------------------------------------------------------------------------------------------------------
  Line   test.php
 ------ ------------------------------------------------------------------------------------------------------------------------------------------------------------
  12     Parameter #1 $impl of method Madbriller\PhpstanRepro\Consumer::call() expects Madbriller\PhpstanRepro\InterfaceExists, Madbriller\PhpstanRepro\Impl given.
 ------ ------------------------------------------------------------------------------------------------------------------------------------------------------------



 [ERROR] Found 1 error
```

However running `php src/test.php` prints "reached".
