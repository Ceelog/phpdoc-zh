可变变量
--------

有时候使用可变变量名是很方便的。就是说，一个变量的变量名可以动态的设置和使用。一个普通的变量通过声明来设置，例如：

``` php
<?php
$a = 'hello';
?>
```

一个可变变量获取了一个普通变量的值作为这个可变变量的变量名。在上面的例子中
*hello*
使用了两个美元符号（$）以后，就可以作为一个可变变量的变量了。例如：

``` php
<?php
$$a = 'world';
?>
```

这时，两个变量都被定义了：`$a` 的内容是“hello”并且 `$hello`
的内容是“world”。因此，以下语句：

``` php
<?php
echo "$a ${$a}";
?>
```

与以下语句输出完全相同的结果：

``` php
<?php
echo "$a $hello";
?>
```

它们都会输出：<span class="computeroutput">hello world</span>。

要将可变变量用于数组，必须解决一个模棱两可的问题。这就是当写下 `$$a[1]`
时，解析器需要知道是想要 `$a[1]` 作为一个变量呢，还是想要 `$$a`
作为一个变量并取出该变量中索引为 \[1\]
的值。解决此问题的语法是，对第一种情况用 `${$a[1]}`，对第二种情况用
`${$a}[1]`。

类的属性也可以通过可变属性名来访问。可变属性名将在该调用所处的范围内被解析。例如，对于
`$foo->$bar` 表达式，则会在本地范围来解析 `$bar` 并且其值将被用于 `$foo`
的属性名。对于 `$bar` 是数组单元时也是一样。

也可使用花括号来给属性名清晰定界。最有用是在属性位于数组中，或者属性名包含有多个部分或者属性名包含有非法字符时（例如来自
<span class="function">json\_decode</span> 或
<a href="/book/simplexml.html" class="link">SimpleXML</a>）。

**示例 \#1 可变属性示例**

``` php
<?php
class foo {
    var $bar = 'I am bar.';
    var $arr = array('I am A.', 'I am B.', 'I am C.');
    var $r   = 'I am r.';
}

$foo = new foo();
$bar = 'bar';
$baz = array('foo', 'bar', 'baz', 'quux');
echo $foo->$bar . "\n";
echo $foo->$baz[1] . "\n";

$start = 'b';
$end   = 'ar';
echo $foo->{$start . $end} . "\n";

$arr = 'arr';
echo $foo->$arr[1] . "\n";
echo $foo->{$arr}[1] . "\n";

?>
```

以上例程会输出：

  
I am bar.  
I am bar.  
I am bar.  
I am r.  
I am B.  

**Warning**

注意，在 PHP
的函数和类的方法中，<a href="/language/variables/superglobals.html" class="link">超全局变量</a>不能用作可变变量。*$this*
变量也是一个特殊变量，不能被动态引用。
