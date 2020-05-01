预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SEEK_SET`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SEEK_CUR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SEEK_END`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`LOCK_SH`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`LOCK_EX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`LOCK_UN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`LOCK_NB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_BRACE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_ONLYDIR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_MARK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_NOSORT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_NOCHECK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_NOESCAPE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`GLOB_AVAILABLE_FLAGS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PATHINFO_DIRNAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PATHINFO_BASENAME`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PATHINFO_EXTENSION`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PATHINFO_FILENAME`** (<span class="type">integer</span>)  
<span class="simpara"> 自 PHP 5.2.0 起 </span>

**`FILE_USE_INCLUDE_PATH`** (<span class="type">integer</span>)  
<span class="simpara"> 在
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
里搜索 `filename`。 (自 PHP 5 起)。 </span>

**`FILE_NO_DEFAULT_CONTEXT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`FILE_APPEND`** (<span class="type">integer</span>)  
<span class="simpara"> 为存在的文件添加内容。 </span>

**`FILE_IGNORE_NEW_LINES`** (<span class="type">integer</span>)  
<span class="simpara"> 过滤换行（EOL）字符（PHP 5 起）。 </span>

**`FILE_SKIP_EMPTY_LINES`** (<span class="type">integer</span>)  
<span class="simpara"> 过滤空行（自 PHP 5 起）。 </span>

**`FILE_BINARY`** (<span class="type">integer</span>)  
二进制模式（自 PHP 5.2.7 起）。

> **Note**:
>
> 此常量无效，仅仅用于向后兼容（*forward compatibility*）。

**`FILE_TEXT`** (<span class="type">integer</span>)  
文本模式 (自 PHP 5.2.7 起)。

> **Note**:
>
> 此常量无效，仅仅用于向后兼容（*forward compatibility*）。

**`INI_SCANNER_NORMAL`** (<span class="type">integer</span>)  
<span class="simpara"> 普通的 INI 扫描模式（自 PHP 5.3 起）。 </span>

**`INI_SCANNER_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> 原始（Raw） INI 扫描模式（自 PHP 5.3 起）。
</span>

**`INI_SCANNER_TYPED`** (<span class="type">integer</span>)  
<span class="simpara"> Typed INI 扫描模式（自 PHP 5.5.6.1 起）。 </span>

**`FNM_NOESCAPE`** (<span class="type">integer</span>)  
<span class="simpara"> 禁用反斜线转义 </span>

**`FNM_PATHNAME`** (<span class="type">integer</span>)  
<span class="simpara"> 字符串里的斜杠只匹配指定模式里的斜杠。 </span>

**`FNM_PERIOD`** (<span class="type">integer</span>)  
<span class="simpara"> 字符串里的起始点号必须完全匹配指定模式里的点号。
</span>

**`FNM_CASEFOLD`** (<span class="type">integer</span>)  
<span class="simpara"> 大小写不敏感的匹配，GNU 扩展的一部分。 </span>
