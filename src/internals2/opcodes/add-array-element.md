ADD\_ARRAY\_ELEMENT
-------------------

PHP code
--------

``` php
<?php
/*
 * Add elem-value as an element to array-value
 * opcode number: 72
 */
$a = array(1,2,3);
print_r($a);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$a

| line | \#  | op                  | fetch | ext | return | operands   |
|------|-----|---------------------|-------|-----|--------|------------|
| 6    | 0   | INIT\_ARRAY         |       |     | \~0    | 1          |
|      | 1   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 2          |
|      | 2   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 3          |
|      | 3   | ASSIGN              |       |     |        | !0,\~0     |
| 7    | 4   | SEND\_VAR           |       |     |        | !0         |
|      | 5   | DO\_FCALL           |       | 1   |        | 'print\_r' |
| 8    | 6   | RETURN              |       |     |        | 1          |
