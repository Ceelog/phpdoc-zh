回调
====

**目录**

-   [结果回调](/memcached/callbacks.html#结果回调)
-   [通读缓存回调](/memcached/callbacks.html#通读缓存回调)

结果回调
--------

Result <span class="type">callbacks</span>方式在通过 <span
class="methodname">Memcached::getDelayed</span>或 <span
class="methodname">Memcached::getDelayedBykey</span>方法获取元素后，为结果集中每个元素调用一次。
回调函数可以接收到一个Memcached对象合一个数组描述的元素信息，此回调函数不需要返回任何信息。

**示例 \#1 结果回调示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$m->getDelayed(array('key1', 'key3'), true, 'result_cb');

function result_cb($memc, $item)
{
    var_dump($item);
}
?>
```

以上例程的输出类似于：

    array(3) {
      ["key"]=>
      string(4) "key1"
      ["value"]=>
      string(6) "value1"
      ["cas"]=>
      float(49)
    }
    array(3) {
      ["key"]=>
      string(4) "key3"
      ["value"]=>
      string(6) "value3"
      ["cas"]=>
      float(50)
    }

通读缓存回调
------------

通读缓存回调在一个元素没有从服务端检索到的时候被调用。这个回调函数会接收到Memcached对象，请求的key以及
一个引用方式传递的值变量等三个参数。此回调函数负责通过返回true或false来决定在key没有值时设置一个默认值。
如果回调返回true，Memcached会存储"传出参数"(引用传递的值变量)存储的值到memcached服务端并将其返回到原来
的调用函数中。仅仅 <span class="methodname">Memcached::get</span>和
<span class="methodname">Memcached::getByKey</span>
支持这类回调，因为Memcache协议不支持在请求多个key时提供未检索到key的信息。

**示例 \#1 通读回调示例**

``` php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$profile_info = $m->get('user:'.$user_id, 'user_info_cb');

function user_info_cb($memc, $key, &$value)
{
    $user_id = substr($key, 5);
    /* 从数据库读取个人信息 */
    /* ... */
    $value = $profile_info;
    return true;
}
?>
```
