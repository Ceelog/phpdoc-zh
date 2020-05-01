对象化接口
----------

对象接口提供一个面向对象的方式来访问扩展接口。下面的例子显示了使用对象化接口实现上面的例子。此例子的输出，除了所显示“计数器无效!”变为由
PHP 发出的变量 *$counter\_three*
不是对象的警告信息以外，其他完全一样。此例子展示了定义在扩展中定义的
<span class="classname">Counter</span>
的子类，并对实例变量而不是用方法存取计数器的值。

**示例 \#1 "counter" 的对象化接口**

``` php
<?php
class MyCounter extends Counter
{
    public function printCounterInfo() {
        printf("计数器的名称为 '%s'，且%s进行持久化。其当前值为 %d.\n",
            $this->getMeta(COUNTER_META_NAME),
            $this->getMeta(COUNTER_META_IS_PERSISTENT) ? '' : '不',
            $this->value);
    }
}

Counter::setCounterClass("MyCounter");
if (($counter_one = Counter::getNamed("one")) === NULL) {
    $counter_one = new Counter("one", 0, COUNTER_FLAG_PERSIST);
}
$counter_one->bumpValue(2); // 不允许直接 "set" 值
$counter_two = new Counter("two", 5);
$counter_three = Counter::getNamed("three");
$counter_four = new Counter("four", 2, COUNTER_FLAG_PERSIST | COUNTER_FLAG_SAVE | COUNTER_FLAG_NO_OVERWRITE);
$counter_four->bumpValue(1);

$counter_one->printCounterInfo();
$counter_two->printCounterInfo();
$counter_three->printCounterInfo();
$counter_four->printCounterInfo();
?>
```
