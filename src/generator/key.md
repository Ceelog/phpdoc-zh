Generator::key
==============

返回当前产生的键

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Generator::key</span> ( <span
class="methodparam">void</span> )

获取产生的值的键

### 参数

此函数没有参数。

### 返回值

返回当前产生的键。

### 范例

**示例 \#1 <span class="methodname">Generator::key</span> example**

``` php
<?php

function Gen()
{
    yield 'key' => 'value';
}

$gen = Gen();

echo "{$gen->key()} => {$gen->current()}";
```

以上例程会输出：

    key => value
