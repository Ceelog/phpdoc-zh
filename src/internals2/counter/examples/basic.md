简单接口
--------

简单接口提供 3 个简单的函数，实例如下：

**示例 \#1 "counter"的简单接口**

``` php
<?php
$starting_counter_value = counter_get();
counter_bump(1);
$second_counter_value = counter_get();
counter_reset();
$final_counter_value = counter_get();
printf("%3d %3d %3d", $starting_counter_value, $second_counter_value, $final_counter_value);
?>
```

以上例程会输出：

      0   1   0

简单接口也提供一系列
<a href="/internals2/counter/constants.html" class="link">INI settings</a>.
