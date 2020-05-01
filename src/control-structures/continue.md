*continue*
----------

*continue*
在循环结构用用来跳过本次循环中剩余的代码并在条件求值为真时开始执行下一次循环。

> **Note**: <span class="simpara"> 注意在 PHP 中
> <a href="/control-structures/switch.html" class="link">switch</a>
> 语句被认为是可以使用 *continue* 的一种循环结构。 </span>

*continue* 接受一个可选的数字参数来决定跳过几重循环到循环结尾。默认值是
*1*，即跳到当前循环末尾。

``` php
<?php
while (list ($key, $value) = each($arr)) {
    if (!($key % 2)) { // skip odd members
        continue;
    }
    do_something_odd($value);
}

$i = 0;
while ($i++ < 5) {
    echo "Outer<br />\n";
    while (1) {
        echo "Middle<br />\n";
        while (1) {
            echo "Inner<br />\n";
            continue 3;
        }
        echo "This never gets output.<br />\n";
    }
    echo "Neither does this.<br />\n";
}
?>
```

省略 *continue* 后面的分号会导致混淆。以下例子示意了不应该这样做。

``` php
<?php
  for ($i = 0; $i < 5; ++$i) {
      if ($i == 2)
          continue
      print "$i\n";
  }
?>
```

希望得到的结果是：

    0
    1
    3
    4

可实际的输出是：

    2

因为整个 *continue print "$i\\n";* 被当做单一的表达式而求值，所以 <span
class="function">print</span> 函数只有在 *$i == 2*
为真时才被调用（*print* 的值被当成了上述的可选数字参数而传递给了
*continue*）。

| 版本  | 说明                                                           |
|-------|----------------------------------------------------------------|
| 5.4.0 | *continue 0;* 不再合法。这在之前的版本被解析为 *continue 1;*。 |
| 5.4.0 | 取消变量作为参数传递（例如 *$num = 2; continue $num;*）。      |
