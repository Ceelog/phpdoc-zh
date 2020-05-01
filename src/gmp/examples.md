范例
====

**示例 \#1 Factorial function using GMP**

``` php
<?php
function fact($x) 
{
    $return = 1;
    for ($i=2; $i <= $x; $i++) {
        $return = gmp_mul($return, $i);
    }
    return $return;
}

echo gmp_strval(fact(1000)) . "\n";
?>
```

This will calculate factorial of 1000 (pretty big number) very fast.
