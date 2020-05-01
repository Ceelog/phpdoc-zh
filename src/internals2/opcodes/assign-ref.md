ASSIGN\_REF
-----------

PHP code
--------

``` php
<?php
/*
 * indicates that variable indicated by value1 is to be treated in the global scope for the remainder of the current scope.
 * opcode number: 39
 */
global $a;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch      | ext | return | operands |
|------|-----|-------------|------------|-----|--------|----------|
| 6    | 0   | FETCH\_W    | globallock |     | $0     | 'a'      |
|      | 1   | ASSIGN\_REF |            |     |        | !0,$0    |
| 7    | 2   | RETURN      |            |     |        | 1        |
