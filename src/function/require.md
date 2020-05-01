require
-------

*require* 和 <span class="function">include</span>
几乎完全一样，除了处理失败的方式不同之外。<span
class="function">require</span> 在出错时产生 **`E_COMPILE_ERROR`**
级别的错误。换句话说将导致脚本中止而 <span
class="function">include</span>
只产生警告（**`E_WARNING`**），脚本会继续运行。

参见 <span class="function">include</span> 文档了解详情。
