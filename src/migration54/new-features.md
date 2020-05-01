新特性
------

PHP 5.4.0 提供了丰富的新特性：

-   <span class="simpara"> 新增支持
    <a href="/language/oop5/traits.html" class="link">traits</a> 。
    </span>
-   <span class="simpara"> 新增短数组语法，比如 *$a = \[1, 2, 3, 4\];*
    或 *$a = \['one' =\> 1, 'two' =\> 2, 'three' =\> 3, 'four' =\> 4\];*
    。 </span>
-   <span class="simpara"> 新增支持对函数返回数组的成员访问解析，例如
    *foo()\[0\]* 。 </span>
-   <span class="simpara"> 现在
    <a href="/functions/anonymous.html" class="link">闭包</a> 支持
    *$this* 。 </span>
-   <span class="simpara"> 现在不管是否设置
    <a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>
    `php.ini` 选项，*\<?=* 将总是可用。 </span>
-   <span class="simpara"> 新增在实例化时访问类成员，例如： *(new
    Foo)-\>bar()* 。 </span>
-   <span class="simpara"> 现在支持 *Class::{expr}()* 语法。 </span>
-   <span class="simpara"> 新增二进制直接量，例如：*0b001001101* 。
    </span>
-   <span class="simpara"> 改进解析错误信息和不兼容参数的警告。 </span>
-   <span class="simpara"> SESSION 扩展现在能追踪文件的
    <a href="/session/upload-progress.html" class="link">上传进度</a> 。
    </span>
-   <span class="simpara"> 内置用于开发的
    <a href="/features/commandline/webserver.html" class="link">CLI 模式的 web server</a>
    。 </span>
