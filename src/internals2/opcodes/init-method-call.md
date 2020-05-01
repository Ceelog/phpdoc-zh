INIT\_METHOD\_CALL
------------------

PHP code
--------

``` php
<?php
/*
 * Prepare for a method call.  Followed by DO_FCALL.
 * opcode number: 112
 */
class A {
  var $num;
    function incrementNum(){
    $num++;
  }
}

$obj = new A();
$obj->incrementNum();

?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$obj

| line | \#  | op                       | fetch | ext | return | operands          |
|------|-----|--------------------------|-------|-----|--------|-------------------|
| 6    | 0   | NOP                      |       |     |        |                   |
| 13   | 1   | ZEND\_FETCH\_CLASS       |       |     | :1     | 'A'               |
|      | 2   | NEW                      |       |     | $2     | :1                |
|      | 3   | DO\_FCALL\_BY\_NAME      |       | 0   |        |                   |
|      | 4   | ASSIGN                   |       |     |        | !0,$2             |
| 14   | 5   | ZEND\_INIT\_METHOD\_CALL |       |     |        | !0,'incrementNum' |
|      | 6   | DO\_FCALL\_BY\_NAME      |       | 0   |        |                   |
| 16   | 7   | RETURN                   |       |     |        | 1                 |

Function name: incrementNum

Compiled variables: !0=$num

| line | \#  | op        | fetch | ext | return | operands |
|------|-----|-----------|-------|-----|--------|----------|
| 9    | 0   | POST\_INC |       |     | \~0    | !0       |
|      | 1   | FREE      |       |     |        | \~0      |
| 10   | 2   | RETURN    |       |     |        | null     |
