预定义变量
----------

PHP
提供了大量的预定义变量。由于许多变量依赖于运行的服务器的版本和设置，及其它因素，所以并没有详细的说明文档。一些预定义变量在
PHP
以<a href="/features/commandline.html" class="link">命令行</a>形式运行时并不生效。有关这些变量的详细列表，请参阅<a href="/reserved/variables.html" class="link">预定义变量</a>一章。

**Warning**

PHP 4.2.0 以及后续版本中，PHP 指令
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
的默认值为 *off*。这是 PHP 的一个主要变化。让 register\_globals 的值为
*off* 将影响到预定义变量集在全局范围内的有效性。例如，为了得到
`DOCUMENT_ROOT` 的值，将必须使用 `$_SERVER['DOCUMENT_ROOT']` 代替
`$DOCUMENT_ROOT`，又如，使用 `$_GET['id']` 来代替 `$id` 从 URL
*http://www.example.com/test.php?id=3* 中获取 id 值，亦或使用
`$_ENV['HOME']` 来代替 `$HOME` 获取环境变量 HOME 的值。

更多相关信息，请阅读
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
的配置项条目，安全一章中的<a href="/security/globals.html" class="link">使用 Register Globals</a>，以及
PHP
<a href="https://www.php.net/releases/4_1_0.php" class="link external">» 4.1.0</a>
和
<a href="https://www.php.net/releases/4_2_0.php" class="link external">» 4.2.0</a>
的发布公告。

如果有可用的 PHP
预定义变量那最好用，如<a href="/language/variables/superglobals.html" class="link">超全局数组</a>。

从 PHP 4.1.0 开始，PHP 提供了一套附加的预定数组，这些数组变量包含了来自
web
服务器（如果可用），运行环境，和用户输入的数据。这些数组非常特别，它们在全局范围内自动生效，例如，在任何范围内自动生效。因此通常被称为自动全局变量（autoglobals）或者超全局变量（superglobals）。（PHP
中没有用户自定义超全局变量的机制。）超全局变量罗列于下文中；但是为了得到它们的内容和关于
PHP
预定义变量的进一步的讨论以及它们的本质，请参阅<a href="/reserved/variables.html" class="link">预定义变量</a>。而且，你也将注意到旧的预定义数组（`$HTTP_*_VARS`）仍旧存在。自
PHP 5.0.0 起, 用
<a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>
设置选项可禁用 长类型的 PHP
<a href="/language/variables/predefined.html" class="link">预定义变量</a>数组。

> **Note**: **可变变量**  
>
> 超级全局变量不能被用作函数或类方法中的<a href="/language/variables/variable.html" class="link">可变变量</a>。

> **Note**:
>
> 尽管超全局变量和 HTTP\_\*\_VARS
> 同时存在，但是它们并不是同一个变量，所以改变其中一个的值并不会对另一个产生影响。

如果某些
<a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
中的变量没有设定，它们的对应的 PHP 预定义数组也是空的。
