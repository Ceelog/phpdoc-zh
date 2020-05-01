IS\_NOT\_EQUAL
--------------

PHP code
--------

``` php
<?php
/*
 * compares if value1 and value2 are not equal
 * opcode number: 18
 */
echo (1 != 1);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op             | fetch | ext | return | operands |
|------|-----|----------------|-------|-----|--------|----------|
| 6    | 0   | IS\_NOT\_EQUAL |       |     | \~0    | 1,1      |
|      | 1   | ECHO           |       |     |        | \~0      |
| 7    | 2   | RETURN         |       |     |        | 1        |
