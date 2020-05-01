SEND\_VAL
---------

PHP code
--------

``` php
<?php
/*
 * Pass the constant value as an actual parameter to a function.  DO_FCALL follows.
 * opcode number: 65
 */
function funcA($msg){
    print $msg;
}

funcA('HELLO');

defined('IN_PHPBB');
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands    |
|------|-----|-----------|-------|-----|--------|-------------|
| 6    | 0   | NOP       |       |     |        |             |
| 10   | 1   | SEND\_VAL |       |     |        | 'HELLO'     |
|      | 2   | DO\_FCALL |       | 1   |        | 'funca'     |
| 12   | 3   | SEND\_VAL |       |     |        | 'IN\_PHPBB' |
|      | 4   | DO\_FCALL |       | 1   |        | 'defined'   |
| 13   | 5   | RETURN    |       |     |        | 1           |

Function name: funcA

Compiled variables: !0=$msg

| line | \#  | op     | fetch | ext | return | operands |
|------|-----|--------|-------|-----|--------|----------|
| 6    | 0   | RECV   |       |     |        | 1        |
| 7    | 1   | PRINT  |       |     | \~0    | !0       |
|      | 2   | FREE   |       |     |        | \~0      |
| 8    | 3   | RETURN |       |     |        | null     |
