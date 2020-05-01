zookeeper\_dispatch
===================

Calls callbacks for pending operations

### 说明

<span class="type">void</span> <span
class="methodname">zookeeper\_dispatch</span> ( <span
class="methodparam">void</span> )

The <span class="function">zookeeper\_dispatch</span> function calls the
callbacks passwd by operations like <span
class="methodname">Zookeeper::get</span> or <span
class="methodname">Zookeeper::exists</span>.

**Caution**

Since version 0.4.0, this function must be called manually to achieve
asynchronous operations. If you want that to be done automatically, you
also can declare ticks at the beginning of your program.

After PHP 7.1, you can ignore this function. This extension uses
EG(vm\_interrupt) to implement async dispatch.

### 错误／异常

This method emits PHP warning when callback could not be invoked.

### 范例

**示例 \#1 <span class="methodname">zookeeper\_dispatch</span> example
\#1**

Dispatch callbacks manually.

``` php
<?php
$client = new Zookeeper();
$client->connect('localhost:2181');
$client->get('/zookeeper', function() {
    echo "Callback was called".PHP_EOL;
});
while(true) {
    sleep(1);
    zookeeper_dispatch();
}
?>
```

**示例 \#2 <span class="methodname">zookeeper\_dispatch</span> example
\#2**

Declare ticks.

``` php
<?php
declare(ticks=1);

$client = new Zookeeper();
$client->connect('localhost:2181');
$client->get('/zookeeper', function() {
    echo "Callback was called".PHP_EOL;
});
while(true) {
    sleep(1);
}
?>
```

### 参见

-   <span class="methodname">Zookeeper::addAuth</span>
-   <span class="methodname">Zookeeper::connect</span>
-   <span class="methodname">Zookeeper::\_\_construct</span>
-   <span class="methodname">Zookeeper::exists</span>
-   <span class="methodname">Zookeeper::get</span>
-   <span class="methodname">Zookeeper::getChildren</span>
-   <span class="methodname">Zookeeper::setWatcher</span>

**目录**

-   [zookeeper\_dispatch](/ref/zookeeper.html#zookeeper_dispatch) —
    Calls callbacks for pending operations
