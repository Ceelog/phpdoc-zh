PHP 和 HTML
===========

PHP 和 HTML 有很多相互作用：PHP 能生成 HTML，HTML 可以向 PHP
传递信息。在阅读这些常见问题之前，先学会怎样
<a href="/language/variables/external.html" class="link">从 PHP 之外取得变量</a>很重要。此主题的手册页也包括很多例子。还要仔细留意
*register\_globals*对你意味着什么。

1.  [当我通过表单／URL
    传值时需要用什么编码／解码方法？](#faq.html.encoding)
2.  [我在试用 \<input type="image"\> 标记，但是没有 $foo.x和
    $foo.y变量，它们哪去了？](#faq.html.form-image)
3.  [怎样在 HTML 的 \<form\> 中建立数组？](#faq.html.arrays)
4.  [怎样从可多选的 HTML 的 select multiple
    标记中得到所有结果？](#faq.html.select-multiple)
5.  [怎样从 Javascript 传递一个变量到
    PHP？](#faq.html.javascript-variable)

**当我通过表单／URL 传值时需要用什么编码／解码方法？**  
在几个环节上编码方式很重要。假定有 <span class="type">string</span>
`$data`，其中包含了想通过非编码方式传递的字符串，那这是相关步骤：

-   HTML 解析。要指定一个任意的字符串， *必须*将其放在双引号中，并用
    <span class="function">htmlspecialchars</span>处理整个值。

-   URL：URL 由几部分组成。如果希望自己的数据被当作其中一项来解释，
    *必须*用 <span class="function">urlencode</span>对其编码。

**示例 \#1 隐藏的 HTML 表单单元**

``` php
<?php
    echo "<input type='hidden' value='" . htmlspecialchars($data) . "' />\n";
?>
```

> **Note**: <span class="simpara">用 <span
> class="function">urlencode</span>来处理
> `$data`是错误的，因为是浏览器的责任来 <span
> class="function">urlencode</span>数据。所有流行的浏览器都能正确处理。注意不论何种方法（例如
> GET 或 POST）都会这样。不过只会在用 GET 请求时注意到这一点，因为 POST
> 请求通常是隐藏的。</span>

**示例 \#2 等待用户编辑的数据**

``` php
<?php
    echo "<textarea name='mydata'>\n";
    echo htmlspecialchars($data)."\n";
    echo "</textarea>";
?>
```

> **Note**: <span
> class="simpara">数据会按照预期的显示在浏览器中，因为浏览器会解释 HTML
> 转义符号。</span> <span class="simpara">当提交时，不论是 GET 或者 POST
> 方法，数据都会被浏览器进行 urlencode 来传输，并直接被 PHP
> urldecode。所以最终不需要自己处理任何
> urlencoding/urldecoding，全都是自动处理的。</span>

**示例 \#3 URL 中的例子**

``` php
<?php
    echo "<a href='" . htmlspecialchars("/nextpage.php?stage=23&data=" .
        urlencode($data)) . "'>\n";
?>
```

> **Note**: <span class="simpara">事实上这在编造一个 HTML 的 GET
> 请求，因此需要手工对数据进行 <span
> class="function">urlencode</span>。</span>

> **Note**: <span class="simpara">需要对整个 URL 进行 <span
> class="function">htmlspecialchars</span>，因为 URL 是作为 HTML
> 属性的一个值出现的。在本例中，浏览器会首先对值进行 un- <span
> class="function">htmlspecialchars</span>，然后再传递此 URL。PHP
> 将能正确理解 URL，因为对数据进行了 <span
> class="function">urlencoded</span>。</span> <span
> class="simpara">要注意到 URL 中的 *&*被替换成了
> *&amp;*。如果忘了这一步，尽管大多数浏览器都能恢复，但也不总是这样。因此即使
> URL 不是动态的，也 *需要*对 URL 进行 <span
> class="function">htmlspecialchars</span>。</span>

<!-- -->

**我在试用 \<input type="image"\> 标记，但是没有 `$foo.x`和 `$foo.y`变量，它们哪去了？**  
当提交表单时，可以用图片代替标准的提交按钮，用类似这样的标记：

``` html
<input type="image" src="image.gif" name="foo" />
```

当用户点击了图片的任何部分，该表单会被发送到服务器并加上两个额外的变量：
`foo.x`和 `foo.y`。

因为 `foo.x`和 `foo.y`在 PHP 中会成为非法的变量名，它们被自动转换成了
`foo_x`和 `foo_y`。也就是用下划线代替了点。因此，可以按照在
<a href="/language/variables/external.html" class="link">来自 PHP 之外的变量</a>这一节中说明的那样访问这些变量。例如，
`$_GET['foo_x']`。

> **Note**:
>
> 请求变量名中的空格被转换为下划线。

<!-- -->

**怎样在 HTML 的 \<form\> 中建立数组？**  
要使你的 \<form\> 结果被当成
<a href="/language/types/array.html" class="link">array</a>发送到 PHP
脚本，要对 \<input\>，\<select\> 或者 \<textarea\> 单元这样命名：

``` html
<input name="MyArray[]" />
<input name="MyArray[]" />
<input name="MyArray[]" />
<input name="MyArray[]" />
```

注意变量名后的方括号，这使其成为一个数组。可以通过给不同的单元分配相同的名字来把单元分组到不同的数组里：

``` html
<input name="MyArray[]" />
<input name="MyArray[]" />
<input name="MyOtherArray[]" />
<input name="MyOtherArray[]" />
```

这将产生两个数组，MyArray 和 MyOtherArray，并发送给 PHP
脚本。还可以给数组分配指定的键名：

``` html
<input name="AnotherArray[]" />
<input name="AnotherArray[]" />
<input name="AnotherArray[email]" />
<input name="AnotherArray[phone]" />
```

AnotherArray 数组将包含键名 0，1，email 和 phone。

> **Note**:
>
> 指定数组的键名是 HTML
> 的可选项。如果不指定键名，则数组被按照单元在表单中出现的顺序填充。第一个例子将包含键名
> 0，1，2 和 3。

参见 <a href="/ref/array.html" class="link">数组函数</a>和
<a href="/language/variables/external.html" class="link">来自 PHP 之外的变量</a>。

<!-- -->

**怎样从可多选的 HTML 的 select multiple 标记中得到所有结果？**  
可多选的 select multiple 标记是 HTML
的一个构造，允许用户从一个列表中选择多个项目。这些项目接着被传递给该表单
action 中指定的处理程序。问题是它们都会被用同样的名字传递。例如：

``` html
<select name="var" multiple="yes">
```

每个被选项将这样被传递到表单处理程序：

    var=option1 var=option2 var=option3

每个选项将覆盖前面一个 `$var`变量的内容。解决方案是用 PHP
的“表单单元数组”特性。使用方法如下：

``` html
<select name="var[]" multiple="yes">
```

这将告诉 PHP 将 `$var`当成数组对待，每个对 var\[\]
的赋值都会给数组增加一项。第一项将成为 `$var[0]`，下一个是
`$var[1]`，等等。可以用 <span
class="function">count</span>函数来测定选择了多少个项目，必要时可以用
<span class="function">sort</span>函数来对选项的数组进行排序。

注意如果在 JavaScript 中通过名字来引用单元，单元名字中的
*\[\]*可能会造成问题。用表单单元中的数字序号来替代，或者将变量名用单引号括起来并用其作为单元数组的索引，例如：

    variable = documents.forms[0].elements['var[]'];

<!-- -->

**怎样从 Javascript 传递一个变量到 PHP？**  
由于 Javascript （通常情况下）是客户端技术，而 PHP
（通常情况下）是服务器端技术，而且 HTTP
是一种“无状态”协议，因此两种语言之间不能直接共享变量。

但是，有可能在二者之间传递变量。一种实现的方法是用 PHP 生成 Javascript
代码，并让浏览器自动刷新，将特定的变量传递回 PHP
脚本。以下例子显示了如何这样做——让 PHP
代码取得显示屏幕的高度和宽度，通常只能在客户端这么做。

``` php
<?php
if (isset($_GET['width']) AND isset($_GET['height'])) {
  // output the geometry variables
  echo "Screen width is: ". $_GET['width'] ."<br />\n";
  echo "Screen height is: ". $_GET['height'] ."<br />\n";
} else {
  // pass the geometry variables
  // (preserve the original query string
  //   -- post variables will need to handled differently)

  echo "<script language='javascript'>\n";
  echo "  location.href=\"${_SERVER['SCRIPT_NAME']}?${_SERVER['QUERY_STRING']}"
            . "&width=\" + screen.width + \"&height=\" + screen.height;\n";
  echo "</script>\n";
  exit();
}
?>
```
