扩展接口
--------

扩展接口提供小的一整套函数，允许用户根据设置定义任意数量名称唯一的计数器。简单接口可与扩展接口同时使用。

**示例 \#1 "counter"的扩展接口**

``` php
<?php
function print_counter_info($counter)
{
    if (is_resource($counter)) {
        printf("计数器的名称为 '%s'，且%s进行持久化。其当前值为 %d.\n",
            counter_get_meta($counter, COUNTER_META_NAME),
            counter_get_meta($counter, COUNTER_META_IS_PERSISTENT) ? '' : '不',
            counter_get_value($counter));
    } else {
      print "计数器无效!\n";
    }
}

if (($counter_one = counter_get_named("one")) === NULL) {
    $counter_one = counter_create("one", 0, COUNTER_FLAG_PERSIST);
}
counter_bump_value($counter_one, 2);
$counter_two = counter_create("two", 5);
$counter_three = counter_get_named("three");
$counter_four = counter_create("four", 2, COUNTER_FLAG_PERSIST | COUNTER_FLAG_SAVE | COUNTER_FLAG_NO_OVERWRITE);
counter_bump_value($counter_four, 1);

print_counter_info($counter_one);
print_counter_info($counter_two);
print_counter_info($counter_three);
print_counter_info($counter_four);
?>
```

首次运行时，以上例子的输出为：

    计数器的名称为 'one'，且进行持久化。其当前值为 2.
    计数器的名称为 'two'，且不进行持久化。其当前值为 5.
    计数器无效!
    计数器的名称为 'four'，且进行持久化。其当前值为 3.

在同一 PHP 实例中第 2 次运行时的输出为:

    计数器的名称为 'one'，且进行持久化。其当前值为 4.
    计数器的名称为 'two'，且不进行持久化。其当前值为 5.
    计数器无效!
    计数器的名称为 'four'，且进行持久化。其当前值为 4.

*在另一个 PHP 实例中*第 3 次运行时的输出为：

    计数器的名称为 'one'，且进行持久化。其当前值为 2.
    计数器的名称为 'two，且不进行持久化。其当前值为 5.
    计数器无效!
    计数器的名称为 'four'，且进行持久化。其当前值为 5.
