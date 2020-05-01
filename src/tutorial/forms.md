PHP 一个很有用的特点体现在它处理 PHP
表单的方式。需要理解的非常重要的原理，是表单的任何元素都在 PHP
脚本中自动生效。请参阅本手册中“<a href="/language/variables/external.html" class="link">PHP 的外部变量</a>”以获取关于在
PHP 中使用表单的详细信息及范例。以下是 HTML 表单的范例：

**示例 \#1 一个简单的 HTML 表单**

``` html
<form action="action.php" method="post">
 <p>姓名: <input type="text" name="name" /></p>
 <p>年龄: <input type="text" name="age" /></p>
 <p><input type="submit" /></p>
</form>
```

该表单中并没有什么特殊的地方，其中没有使用任何特殊的标识符。当用户填写了该表单并点击了提交按钮，页面
`action.php` 将被调用。在该文件中，可以加入如下内容：

**示例 \#2 打印来自表单的数据**

``` php
你好，<?php echo htmlspecialchars($_POST['name']); ?>。
你 <?php echo (int)$_POST['age']; ?> 岁了。
```

该脚本的输出可能是：

    你好，Joe。你 22 岁了。

除了<span class="function">htmlspecialchars</span> 和 *(int)*
部分，这段程序做什么用显而易见。<span
class="function">htmlspecialchars</span> 使得 HTML
之中的特殊字符被正确的编码，从而不会被使用者在页面注入 HTML 标签或者
Javascript 代码。例如 age
字段，我们明确知道他是一个数值，因此我们将它<a href="/language/types/type-juggling.html#language.types.typecasting" class="link">转换</a>为一个<span
class="type">整形值(integer)</span>来自动的消除任何不必要的字符。也可以使用
PHP 的 <a href="/ref/filter.html" class="link">filter</a>
扩展来自动完成该工作。PHP 将自动设置 `$_POST['name']` 和 `$_POST['age']`
变量。在这之前我们使用了超全局变量 `$_SERVER`，现在我们引入了超全局变量
<a href="/reserved/variables/post.html" class="link">$_POST</a>，它包含了所有的
POST 数据。请注意我们的表单提交数据的*方法*（method）。如果使用了 *GET*
方法，那么表单中的信息将被储存到超全局变量
<a href="/reserved/variables/get.html" class="link">$_GET</a>
中。如果并不关心请求数据的来源，也可以用超全局变量
<a href="/reserved/variables/request.html" class="link">$_REQUEST</a>，它包含了所有
GET、POST、COOKIE 和 FILE 的数据。

也可以在 PHP 中处理 XForms
的输入，尽管用户可能更喜欢使用长久以来支持良好的 HTML 表单。XForms
目前还不适合初学者使用，但是用户可能对它感兴趣。手册中在“特点”一章有一节对如何<a href="/features/xforms.html" class="link">处理从 XForum 接收到的数据</a>进行了简短的介绍。
