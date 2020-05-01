FETCH\_DIM\_RW
--------------

PHP code
--------

``` php
<?php
/*
 * Fetch the value of the element at "index" in "array-value" to store it in "result".
 * opcode number: 87
 */
$x = array(1,2,3);
$a = 'x';
$$a[0]++;
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: !0=$x, !1=$a

| line | \#  | op                  | fetch | ext | return | operands |
|------|-----|---------------------|-------|-----|--------|----------|
| 6    | 0   | INIT\_ARRAY         |       |     | \~0    | 1        |
|      | 1   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 2        |
|      | 2   | ADD\_ARRAY\_ELEMENT |       |     | \~0    | 3        |
|      | 3   | ASSIGN              |       |     |        | !0,\~0   |
| 7    | 4   | ASSIGN              |       |     |        | !1,'x'   |
| 8    | 5   | FETCH\_DIM\_R       |       |     | $3     | !1,0     |
|      | 6   | FETCH\_RW           | local |     | $4     | $3       |
|      | 7   | POST\_INC           |       |     | \~5    | $4       |
|      | 8   | FREE                |       |     |        | \~5      |
| 9    | 9   | RETURN              |       |     |        | 1        |
