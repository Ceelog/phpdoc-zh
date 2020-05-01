BOOL\_NOT
---------

PHP code
--------

``` php
<?php
/*
 * Boolean (logical) not of "value"
 * opcode number: 13
 */
echo !1;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | BOOL\_NOT |       |     | \~0    | 1        |
|      | 1   | ECHO      |       |     |        | \~0      |
| 7    | 2   | RETURN    |       |     |        | 1        |
