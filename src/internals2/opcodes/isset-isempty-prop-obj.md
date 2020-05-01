ISSET\_ISEMPTY\_PROP\_OBJ
-------------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 148
 */
$obj = new A();
if(empty($obj->num)) return 0;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj

| line | \#  | op                              | fetch | ext | return | operands |
|------|-----|---------------------------------|-------|-----|--------|----------|
| 6    | 0   | ZEND\_FETCH\_CLASS              |       |     | :0     | 'A'      |
|      | 1   | NEW                             |       |     | $1     | :0       |
|      | 2   | DO\_FCALL\_BY\_NAME             |       | 0   |        |          |
|      | 3   | ASSIGN                          |       |     |        | !0,$1    |
| 7    | 4   | ZEND\_ISSET\_ISEMPTY\_PROP\_OBJ |       |     | \~4    | !0,'num' |
|      | 5   | JMPZ                            |       |     |        | \~4,-\>8 |
|      | 6   | RETURN                          |       |     |        | 0        |
|      | 7   | JMP                             |       |     |        | -\>8     |
| 8    | 8   | RETURN                          |       |     |        | 1        |
