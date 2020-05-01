预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`FILEINFO_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> 无特殊处理。 </span>

**`FILEINFO_SYMLINK`** (<span class="type">integer</span>)  
<span class="simpara"> 跟随符号链接。 </span>

**`FILEINFO_MIME_TYPE`** (<span class="type">integer</span>)  
<span class="simpara"> 返回 mime 类型。 </span> <span class="simpara">
自 PHP 5.3.0 可用。 </span>

**`FILEINFO_MIME_ENCODING`** (<span class="type">integer</span>)  
<span class="simpara"> 返回文件的 mime 编码。 </span> <span
class="simpara"> 自 PHP 5.3.0 可用。 </span>

**`FILEINFO_MIME`** (<span class="type">integer</span>)  
<span class="simpara"> 按照 RFC 2045 定义的格式返回文件 mime
类型和编码。 </span>

**`FILEINFO_COMPRESS`** (<span class="type">integer</span>)  
<span class="simpara"> 解压缩压缩文件。 </span> <span class="simpara">
由于线程安全问题，自 PHP 5.3.0 禁用。 </span>

**`FILEINFO_DEVICES`** (<span class="type">integer</span>)  
<span class="simpara"> 查看设备的块内容或字符。 </span>

**`FILEINFO_CONTINUE`** (<span class="type">integer</span>)  
<span class="simpara"> 返回全部匹配的类型。 </span>

**`FILEINFO_PRESERVE_ATIME`** (<span class="type">integer</span>)  
<span class="simpara"> 如果可以的话，尽可能保持原始的访问时间。 </span>

**`FILEINFO_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> 对于不可打印字符不转换成 *\\ooo* 八进制表示格式。
</span>

**`FILEINFO_EXTENSION`** (<span class="type">integer</span>)  
<span class="simpara"> 根据 MIME 类型返回适当的文件扩展名。 </span>
<span class="simpara"> 有的文件类型具有多种扩展名，例如 *JPEG*
将会返回多个扩展名， 以斜杠分隔，比如 *"jpeg/jpg/jpe/jfif"*。 如果在
`magic.mime` 数据库里类型未知，则返回的是 *"???"*。 </span> <span
class="simpara"> PHP 7.2.0 起有效。 </span>
