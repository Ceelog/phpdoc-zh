CAST
----

PHP code
--------

``` php
<?php
/*
 * casts value1 as type value2 (type in extended_value)
 * opcode number: 21
 */
echo (int)1;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | CAST   |       | 4   | \~0    | 1        |
|      | 1   | ECHO   |       |     |        | \~0      |
| 7    | 2   | RETURN |       |     |        | 1        |
