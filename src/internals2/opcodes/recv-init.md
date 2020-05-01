RECV\_INIT
----------

PHP code
--------

``` php
<?php
/*
 * Initialize a function argument with "value" if not received from caller.  Otherwise same as RECV.
 * opcode number: 64
 */
function hello($a=5){}
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

| line | \#  | op         | fetch | ext | return | operands |
|------|-----|------------|-------|-----|--------|----------|
| 6    | 0   | RECV\_INIT |       |     |        | 1,5      |
|      | 1   | RETURN     |       |     |        | null     |
