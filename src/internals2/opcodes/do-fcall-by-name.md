DO\_FCALL\_BY\_NAME
-------------------

PHP code
--------

``` php
<?php
/*
 * Call a function by name.  Following INIT_FCALL_BY_NAME and multiple SEND_VAL, SEND_VAR or SEND_REF.
 * opcode number: 61
 */
$x = 'phpinfo';
$a = $x();
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op                    | fetch | ext | return | operands     |
|------|-----|-----------------------|-------|-----|--------|--------------|
| 6    | 0   | ASSIGN                |       |     |        | !0,'phpinfo' |
| 7    | 1   | INIT\_FCALL\_BY\_NAME |       |     |        | !0           |
|      | 2   | DO\_FCALL\_BY\_NAME   |       | 0   |        |              |
|      | 3   | ASSIGN                |       |     |        | !1,$1        |
| 8    | 4   | RETURN                |       |     |        | 1            |
