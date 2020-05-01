ADD\_VAR
--------

PHP code
--------

``` php
<?php
/*
 * add contents of variable in value2 to string value1 and store in result
 * opcode number: 56
 */
echo "hello$a world";
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op          | fetch | ext | return | operands     |
|------|-----|-------------|-------|-----|--------|--------------|
| 6    | 0   | ADD\_STRING |       |     | \~0    | 'hello'      |
|      | 1   | ADD\_VAR    |       |     | \~0    | \~0,!0       |
|      | 2   | ADD\_STRING |       |     | \~0    | \~0,'+world' |
|      | 3   | ECHO        |       |     |        | \~0          |
| 7    | 4   | RETURN      |       |     |        | 1            |
