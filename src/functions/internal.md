内部（内置）函数
----------------

PHP 有很多标准的函数和结构。还有一些函数需要和特定地 PHP
扩展模块一起编译，否则在使用它们的时候就会得到一个致命的“未定义函数”错误。例如，要使用
<a href="/ref/image.html" class="link">image</a> 函数中的 <span
class="function">imagecreatetruecolor</span>，需要在编译 PHP 的时候加上
<span class="productname">GD</span> 的支持。或者，要使用 <span
class="function">mysqli\_connect</span> 函数，就需要在编译 PHP
的时候加上 <a href="/set/mysqlinfo.html#Mysqli" class="link">MySQLi</a>
支持。有很多核心函数已包含在每个版本的 PHP
中如<a href="/ref/strings.html" class="link">字符串</a>和<a href="/ref/var.html" class="link">变量</a>函数。调用
<span class="function">phpinfo</span> 或者 <span
class="function">get\_loaded\_extensions</span> 可以得知 PHP
加载了那些扩展库。同时还应该注意，很多扩展库默认就是有效的。PHP
手册按照不同的扩展库组织了它们的文档。请参阅<a href="/configuration.html" class="link">配置</a>，<a href="/install.html" class="link">安装</a>以及各自的扩展库章节以获取有关如何设置
PHP 的信息。

手册中<a href="/about/prototypes.html" class="link">如何阅读函数原型</a>讲解了如何阅读和理解一个函数的原型。确认一个函数将返回什么，或者函数是否直接作用于传递的参数是很重要的。例如，<span
class="function">str\_replace</span> 函数将返回修改过的字符串，而 <span
class="function">usort</span>
却直接作用于传递的参数变量本身。手册中，每一个函数的页面中都有关于函数参数、行为改变、成功与否的返回值以及使用条件等信息。了解这些重要的（常常是细微的）差别是编写正确的
PHP 代码的关键。

> **Note**: <span class="simpara">
> 如果传递给函数的参数类型与实际的类型不一致，例如将一个 <span
> class="type">array</span> 传递给一个 <span class="type">string</span>
> 类型的变量，那么函数的返回值是不确定的。在这种情况下，通常函数会返回
> **`NULL`**。但这仅仅是一个惯例，并不一定如此。 </span>

参见 <span
class="function">function\_exists</span>，<a href="/funcref.html" class="link">函数参考</a>，<span
class="function">get\_extension\_funcs</span> 和 <span
class="function">dl</span>。
