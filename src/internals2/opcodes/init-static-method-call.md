INIT\_STATIC\_METHOD\_CALL
--------------------------

PHP code
--------

``` php
<?php
/*
 * 
 * opcode number: 113
 */
class Foo {
    public static function aStaticMethod() {
            echo "hello world\n";
    }
}

Foo::aStaticMethod();
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                               | fetch | ext | return | operands                 |
|------|-----|----------------------------------|-------|-----|--------|--------------------------|
| 6    | 0   | NOP                              |       |     |        |                          |
| 12   | 1   | ZEND\_INIT\_STATIC\_METHOD\_CALL |       |     |        | 'Foo','aStaticMethod'    |
|      | 2   | ZEND\_OP\_DATA                   |       |     |        | 'foo%3A%3Aastaticmethod' |
|      | 3   | DO\_FCALL\_BY\_NAME              |       | 0   |        |                          |
| 13   | 4   | RETURN                           |       |     |        | 1                        |

Function name: aStaticMethod

Compiled variables: none

| line | \#  | op     | fetch | ext | return | operands         |
|------|-----|--------|-------|-----|--------|------------------|
| 8    | 0   | ECHO   |       |     |        | 'hello+world%0A' |
| 9    | 1   | RETURN |       |     |        | null             |
