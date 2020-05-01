ADD\_INTERFACE
--------------

PHP code
--------

``` php
<?php 
/*
 * adds an implemented interface to a class declaration
 * opcode number: 144
 */
interface iA {
}

class A implements iA {
}
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op                      | fetch | ext | return | operands |
|------|-----|-------------------------|-------|-----|--------|----------|
| 6    | 0   | NOP                     |       |     |        |          |
|      | 1   | DECLARE\_CLASS          |       |     |        | 'a'      |
|      | 2   | ADD\_INTERFACE          |       |     |        | 'iA'     |
|      | 3   | VERIFY\_ABSTRACT\_CLASS |       |     |        |          |
|      | 3   | RETURN                  |       |     |        | 1        |
