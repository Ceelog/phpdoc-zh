INSTANCEOF
----------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 138
 */
$obj = new A();

if ($obj instanceof A) {
   echo 'A';
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS  |       |     | :0     | 'A'      |
|      | 1   | NEW                 |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME |       | 0   |        |          |
|      | 3   | ASSIGN              |       |     |        | !0,$1    |
| 8    | 4   | ZEND\_FETCH\_CLASS  |       |     | :4     | 'A'      |
|      | 5   | ZEND\_INSTANCEOF    |       |     | \~5    | !0,$4    |
|      | 6   | JMPZ                |       |     |        | \~5,-\>9 |
| 9    | 7   | ECHO                |       |     |        | 'A'      |
| 10   | 8   | JMP                 |       |     |        | -\>9     |
| 11   | 9   | RETURN              |       |     |        | 1        |
