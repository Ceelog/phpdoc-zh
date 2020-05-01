EXIT
----

PHP code
--------

``` php
<?php
/*
 * Exit running after dumping "message".
 * opcode number: 79
 */
die("foobar");
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | EXIT   |       |     |        | 'foobar' |
| 7    | 1   | RETURN |       |     |        | 1        |
