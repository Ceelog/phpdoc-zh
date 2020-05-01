DO\_FCALL
---------

PHP code
--------

``` php
<?php
/*
 * Call a function.  Following multiple SEND_VAL, SEND_VAR or SEND_REF.
 * opcode number: 60
 */
$a = phpinfo();
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op        | fetch | ext | return | operands  |
|------|-----|-----------|-------|-----|--------|-----------|
| 6    | 0   | DO\_FCALL |       | 0   |        | 'phpinfo' |
|      | 1   | ASSIGN    |       |     |        | !0,$0     |
| 7    | 2   | RETURN    |       |     |        | 1         |
