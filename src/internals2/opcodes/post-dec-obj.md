POST\_DEC\_OBJ
--------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 135
 */
$obj = new A();
$obj->num--;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj

| line | \#  | op                   | fetch | ext | return | operands |
|------|-----|----------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS   |       |     | :0     | 'A'      |
|      | 1   | NEW                  |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME  |       | 0   |        |          |
|      | 3   | ASSIGN               |       |     |        | !0,$1    |
| 7    | 4   | ZEND\_POST\_DEC\_OBJ |       |     | \~5    | !0,'num' |
|      | 5   | FREE                 |       |     |        | \~5      |
| 8    | 6   | RETURN               |       |     |        | 1        |
