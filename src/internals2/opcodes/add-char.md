ADD\_CHAR
---------

PHP code
--------

``` php
<?php
/*
 * add regular characters in encapsed string
 * opcode number: 54
 */
echo "$a ";
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 6    | 0   | ADD\_VAR  |       |     |        | !0       |
|      | 1   | ADD\_CHAR |       |     |        | 32       |
|      | 2   | ECHO      |       |     |        |          |
|      | 3   | RETURN    |       |     |        | 1        |
