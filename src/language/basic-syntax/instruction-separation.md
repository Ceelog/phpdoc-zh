指令分隔符
----------

同 C 或 Perl 一样，PHP 需要在每个语句后用分号结束指令。一段 PHP
代码中的结束标记隐含表示了一个分号；在一个 PHP
代码段中的最后一行可以不用分号结束。如果后面还有新行，则代码段的结束标记包含了行结束。

``` php
<?php
    echo "This is a test";
?>

<?php echo "This is a test" ?>

<?php echo 'We omitted the last closing tag';
```

> **Note**:
>
> 文件末尾的 PHP 代码段结束标记可以不要，有些情况下当使用 <span
> class="function">include</span> 或者 <span
> class="function">require</span>
> 时省略掉会更好些，这样不期望的空白符就不会出现在文件末尾，之后仍然可以输出响应标头。在使用输出缓冲时也很便利，就不会看到由包含文件生成的不期望的空白符。
