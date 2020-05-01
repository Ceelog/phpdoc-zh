POST\_DEC
---------

PHP code
--------

``` php
<?php
/*
 * decrements variable indicated by value1 by 1 (after performing other operations) and stores in result
 * opcode number: 37
 */
$a--;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | POST\_DEC |       |     | \~0    | !0       |
|      | 1   | FREE      |       |     |        | \~0      |
| 7    | 2   | RETURN    |       |     |        | 1        |
