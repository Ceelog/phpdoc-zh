范例
====

**目录**

-   [](/memcache/examples.html#)

**示例 \#1 memcache扩展概览示例**

在这个例子中，一个对象被保存到缓存中，又被取回。对象和其他非标量类型在存储
之前会先被序列化，因此它不可以用来存储资源类型（连接标记及其他）。（译注：请注意隐式的
资源类型存储，比如要保存的对象自身不是资源，但其中某个属性却是资源）

``` php
<?php

$memcache = new Memcache;
$memcache->connect('localhost', 11211) or die ("Could not connect");

$version = $memcache->getVersion();
echo "服务端版本信息: ".$version."<br/>\n";

$tmp_object = new stdClass;
$tmp_object->str_attr = 'test';
$tmp_object->int_attr = 123;

$memcache->set('key', $tmp_object, false, 10) or die ("Failed to save data at the server");
echo "将数据保存到缓存中（数据10秒后失效）<br/>\n";

$get_result = $memcache->get('key');
echo "从缓存中取到的数据:<br/>\n";

var_dump($get_result);

?>
```

**示例 \#2 使用memcache的session处理器**

``` php
<?php

$session_save_path = "tcp://$host:$port?persistent=1&weight=2&timeout=2&retry_interval=10,  ,tcp://$host:$port  ";
ini_set('session.save_handler', 'memcache');
ini_set('session.save_path', $session_save_path);

?>
```
