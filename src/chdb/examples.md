范例
====

**示例 \#1 Creating a chdb file**

``` php
<?php

$data = array(
    'key1' => 'value1',
    'key2' => 'value2',
    // ...
);
chdb_create('data.chdb', $data);

?>
```

The above example will generate a chdb file named *data.chdb* and
containing the key-value pairs defined in `$data`.

**示例 \#2 Loading and looking up a chdb file**

``` php
<?php

$chdb = new chdb('data.chdb');
$value1 = $chdb->get('key1');
$value2 = $chdb->get('key2');

echo $value1, PHP_EOL;
echo $value2, PHP_EOL;

?>
```

以上例程的输出类似于：

    value1
    value2
