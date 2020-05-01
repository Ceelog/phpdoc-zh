SEND\_REF
---------

PHP code
--------

``` php
<?php
/*
 * Pass the reference value as an actual parameter to a function.  DO_FCALL follows.
 * opcode number: 67
 */
@each($input);
?>
```

PHP opcodes
-----------

Function name: (null)

Compiled variables: none

| line | \#  | op             | fetch | ext | return | operands |
|------|-----|----------------|-------|-----|--------|----------|
| 6    | 0   | BEGIN\_SILENCE |       |     | \~0    |          |
|      | 1   | FETCH\_W       | local |     | $1     | 'input'  |
|      | 2   | SEND\_REF      |       |     |        | $1       |
|      | 3   | DO\_FCALL      |       | 1   |        | 'each'   |
|      | 4   | END\_SILENCE   |       |     |        | \~0      |
| 7    | 5   | RETURN         |       |     |        | 1        |
