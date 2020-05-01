范例
====

**示例 \#1 Vector**

``` php
<?php

$vector = new \Ds\Vector();

$vector->push('a');
$vector->push('b', 'c');

$vector[] = 'd';

print_r($vector);

?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
    )

**示例 \#2 Map**

``` php
<?php

$map = new \Ds\Map();

$map->put('a', 1);
$map->put('b', 2);

$map['c'] = 3;

print_r($map);

?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )
