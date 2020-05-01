SEND\_VAR
---------

PHP code
--------

``` php
<?php
/*
 * Pass the variable value as an actual parameter to a function.  DO_FCALL follows.
 * opcode number: 66
 */
$a = array(1,2,3);
if(is_array($a)){ return 0; }
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                  | fetch | ext | return | operands    |
|------|-----|---------------------|-------|-----|--------|-------------|
| 6    | 0   | INIT\_ARRAY         |       |     | \~0    | 1           |
|      | 1   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 2           |
|      | 2   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 3           |
|      | 3   | ASSIGN              |       |     |        | !0,\~0      |
| 7    | 4   | SEND\_VAR           |       |     |        | !0          |
|      | 5   | DO\_FCALL           |       | 1   |        | 'is\_array' |
|      | 6   | JMPZ                |       |     |        | $2,-\>9     |
|      | 7   | RETURN              |       |     |        | 0           |
|      | 8   | JMP                 |       |     |        | -\>9        |
| 8    | 9   | RETURN              |       |     |        | 1           |
