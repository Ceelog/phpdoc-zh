END\_SILENCE
------------

PHP code
--------

``` php
<?php
/*
 * no longer surpress error messages
 * opcode number: 58
 */
$my_file = @file ('non_existent_file') or
   die ("error:'$php_errormsg'");
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$my\_file, !1=$php\_errormsg

| line | \#  | op             | fetch | ext | return | operands              |
|------|-----|----------------|-------|-----|--------|-----------------------|
| 6    | 0   | BEGIN\_SILENCE |       |     | \~0    |                       |
|      | 1   | SEND\_VAL      |       |     |        | 'non\_existent\_file' |
|      | 2   | DO\_FCALL      |       | 1   |        | 'file'                |
|      | 3   | END\_SILENCE   |       |     |        | \~0                   |
|      | 4   | ASSIGN         |       |     | $2     | !0,$1                 |
|      | 5   | JMPNZ\_EX      |       |     | \~3    | $2,-\>11              |
| 7    | 6   | ADD\_STRING    |       |     | \~4    | 'error%3A%27'         |
|      | 7   | ADD\_VAR       |       |     | \~4    | \~4,!1                |
|      | 8   | ADD\_CHAR      |       |     | \~4    | \~4,39                |
|      | 9   | EXIT           |       |     |        | \~4                   |
|      | 10  | BOOL           |       |     | \~3    | true                  |
|      | 11  | FREE           |       |     |        | \~3                   |
| 8    | 12  | RETURN         |       |     |        | 1                     |
