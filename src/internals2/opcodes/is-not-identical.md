IS\_NOT\_IDENTICAL
------------------

PHP code
--------

``` php
<?php
/*
 * compares value1 and value2 to see if they are unequal or of different types
 * opcode number: 16
 */
echo (1 !== 1);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                 | fetch | ext | return | operands |
|------|-----|--------------------|-------|-----|--------|----------|
| 6    | 0   | IS\_NOT\_IDENTICAL |       |     | \~0    | 1,1      |
|      | 1   | ECHO               |       |     |        | \~0      |
| 7    | 2   | RETURN             |       |     |        | 1        |
