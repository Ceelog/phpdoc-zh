IS\_SMALLER
-----------

PHP code
--------

``` php
<?php
/*
 * compares if value1 is less than value2
 * opcode number: 19
 */
echo (1 < 2);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op          | fetch | ext | return | operands |
|------|-----|-------------|-------|-----|--------|----------|
| 6    | 0   | IS\_SMALLER |       |     | \~0    | 1,2      |
|      | 1   | ECHO        |       |     |        | \~0      |
| 7    | 2   | RETURN      |       |     |        | 1        |
