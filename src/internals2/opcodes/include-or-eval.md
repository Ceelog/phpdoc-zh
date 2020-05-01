INCLUDE\_OR\_EVAL
-----------------

PHP code
--------

``` php
<?php
/*
 * Include the file specified by filename and eval it.
 * opcode number: 73
 */
include("test.php");
eval("test.php");
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                | fetch | ext | return | operands           |
|------|-----|-------------------|-------|-----|--------|--------------------|
| 6    | 0   | INCLUDE\_OR\_EVAL |       |     |        | 'test.php',INCLUDE |
| 7    | 1   | INCLUDE\_OR\_EVAL |       |     |        | 'test.php',EVAL    |
| 8    | 2   | RETURN            |       |     |        | 1                  |

Function name: (null)

Compiled variables: none

| line | \#  | op        | fetch | ext | return | operands  |
|------|-----|-----------|-------|-----|--------|-----------|
| 2    | 0   | DO\_FCALL |       | 0   |        | 'phpinfo' |
| 3    | 1   | RETURN    |       |     |        | 1         |
