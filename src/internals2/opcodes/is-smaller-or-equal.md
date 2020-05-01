IS\_SMALLER\_OR\_EQUAL
----------------------

PHP code
--------

``` php
<?php
/*
 * compares if value1 is less than or equal to value2
 * opcode number: 20
 */
echo (2 <= 1);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                     | fetch | ext | return | operands |
|------|-----|------------------------|-------|-----|--------|----------|
| 6    | 0   | IS\_SMALLER\_OR\_EQUAL |       |     | \~0    | 2,1      |
|      | 1   | ECHO                   |       |     |        | \~0      |
| 7    | 2   | RETURN                 |       |     |        | 1        |
