return
------

如果在一个函数中调用 <span class="function">return</span>
语句，将立即结束此函数的执行并将它的参数作为函数的值返回。<span
class="function">return</span> 也会终止 <span
class="function">eval</span> 语句或者脚本文件的执行。

如果在全局范围中调用，则当前脚本文件中止运行。如果当前脚本文件是被 <span
class="function">include</span> 的或者 <span
class="function">require</span>
的，则控制交回调用文件。此外，如果当前脚本是被 <span
class="function">include</span> 的，则 <span
class="function">return</span> 的值会被当作 <span
class="function">include</span> 调用的返回值。如果在主脚本文件中调用
<span
class="function">return</span>，则脚本中止运行。如果当前脚本文件是在
`php.ini` 中的配置选项
<a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a>
或者
<a href="/ini/core.html#ini.auto-append-file" class="link">auto_append_file</a>
所指定的，则此脚本文件中止运行。

更多信息见<a href="/functions/returning-values.html" class="link">返回值</a>。

> **Note**: <span class="simpara"> 注意既然 <span
> class="function">return</span>
> 是语言结构而不是函数，因此其参数没有必要用括号将其括起来。通常都不用括号，实际上也应该不用，这样可以降低
> PHP 的负担。 </span>

> **Note**: <span class="simpara">
> 如果没有提供参数，则一定不能用括号，此时返回 **`NULL`**。如果调用
> *return* 时加上了括号却又没有参数会导致解析错误。 </span>

> **Note**: <span class="simpara">
> 当用引用返回值时*永远不要*使用括号，这样行不通。只能通过引用返回变量，而不是语句的结果。如果使用
> *return ($a);* 时其实不是返回一个变量，而是表达式 *($a)*
> 的值（当然，此时该值也正是 `$a` 的值）。 </span>
