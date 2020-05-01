IS\_EQUAL
---------

PHP code
--------

``` php
<?php
/*
 * compares if value1 and value2 are equal
 * opcode number: 17
 */
echo (1 == 1);
echo (1 == 'c');
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | IS\_EQUAL |       |     | \~0    | 1,1      |
|      | 1   | ECHO      |       |     |        | \~0      |
| 7    | 2   | IS\_EQUAL |       |     | \~1    | 1,'c'    |
|      | 3   | ECHO      |       |     |        | \~1      |
| 8    | 4   | RETURN    |       |     |        | 1        |
