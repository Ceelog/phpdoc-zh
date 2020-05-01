预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`XDIFF_PATCH_NORMAL`** (<span class="type">integer</span>)  
<span class="simpara"> This flag indicates that <span
class="function">xdiff\_string\_patch</span> and <span
class="function">xdiff\_file\_patch</span> functions should create
result by applying patch to original content thus creating newer version
of file. This is the default mode of operation. </span>

**`XDIFF_PATCH_REVERSE`** (<span class="type">integer</span>)  
<span class="simpara"> This flag indicated that <span
class="function">xdiff\_string\_patch</span> and <span
class="function">xdiff\_file\_patch</span> functions should create
result by reversing patch changed from newer content thus creating
original version. </span>
