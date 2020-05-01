DECLARE\_INHERITED\_CLASS
-------------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 140
 */
 if($b){
 class Foo {
  public static $my_static = 'foo';
  public function staticValue() {
    return self::$my_static;
  }
 }

 class Bar extends Foo {
  public function fooStatic() {
     echo parent::$my_static;
  }
 }
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$b

| line | \#  | op                              | fetch | ext | return | operands                                                                                                              |
|------|-----|---------------------------------|-------|-----|--------|-----------------------------------------------------------------------------------------------------------------------|
| 6    | 0   | JMPZ                            |       |     |        | !0,-\>5                                                                                                               |
| 7    | 1   | ZEND\_DECLARE\_CLASS            |       |     | $0     | '%00foo%2Fmnt%2Fworkspace%2Fws\_phpscripts%2FPHPopcodes%2Fphpsamples%2FDECLARE\_INHERITED\_CLASS.php0xb7be503b','foo' |
| 14   | 2   | ZEND\_FETCH\_CLASS              |       |     | :1     | 'Foo'                                                                                                                 |
|      | 3   | ZEND\_DECLARE\_INHERITED\_CLASS |       |     | $2     | '%00bar%2Fmnt%2Fworkspace%2Fws\_phpscripts%2FPHPopcodes%2Fphpsamples%2FDECLARE\_INHERITED\_CLASS.php0xb7be50bc','bar' |
| 19   | 4   | JMP                             |       |     |        | -\>5                                                                                                                  |
| 20   | 5   | RETURN                          |       |     |        | 1                                                                                                                     |

Function name: staticValue

Compiled variables: !0=$my\_static

| line | \#  | op                 | fetch        | ext | return | operands     |
|------|-----|--------------------|--------------|-----|--------|--------------|
| 10   | 0   | ZEND\_FETCH\_CLASS |              |     |        |              |
|      | 1   | FETCH\_R           | staticmember |     | $1     | 'my\_static' |
|      | 2   | RETURN             |              |     |        | $1           |
| 11   | 3   | RETURN             |              |     |        | null         |

Function name: fooStatic

Compiled variables: !0=$my\_static

| line | \#  | op                 | fetch        | ext | return | operands     |
|------|-----|--------------------|--------------|-----|--------|--------------|
| 16   | 0   | ZEND\_FETCH\_CLASS |              |     | :0     |              |
|      | 1   | FETCH\_R           | staticmember |     | $1     | 'my\_static' |
|      | 2   | ECHO               |              |     |        | $1           |
| 17   | 3   | RETURN             |              |     |        | null         |
