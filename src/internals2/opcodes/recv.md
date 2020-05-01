RECV
----

PHP code
--------

``` php
<?php
/*
 * Receive a functoin argument of "argument-number" and store the argument value into a variable of "argument-number".  (e.g. $1 for 1)
 * opcode number: 63
 */
function hello($a){}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | NOP    |       |     |        |          |
| 7    | 1   | RETURN |       |     |        | 1        |

Function name: hello

Compiled variables: !0=$a

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | RECV   |       |     |        | 1        |
|      | 1   | RETURN |       |     |        | null     |
