预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

<span class="classname">ZipArchive</span> 使用的类常量。
有以下三类常量：Flags（以 *FL\_* 为前缀），errors（以 *ER\_*
为前缀）以及 mode（没有前缀）。

**`ZIPARCHIVE::CREATE`** (<span class="type">integer</span>)  
<span class="simpara"> 如果不存在则创建一个zip压缩包。 </span>

**`ZIPARCHIVE::OVERWRITE`** (<span class="type">integer</span>)  
<span class="simpara">
总是以一个新的压缩包开始，此模式下如果已经存在则会被覆盖。 </span>

**`ZIPARCHIVE::EXCL`** (<span class="type">integer</span>)  
<span class="simpara"> 如果压缩包已经存在，则出错。 </span>

**`ZipArchive::RDONLY`** (<span class="type">integer</span>)  
<span class="simpara"> 只读模式打开压缩包。 Available as of PHP 7.4.3
and PECL zip 1.17.1, respectively, if built against libzip ≥ 1.0.0.
</span>

**`ZIPARCHIVE::CHECKCONS`** (<span class="type">integer</span>)  
<span class="simpara">
对压缩包执行额外的一致性检查，如果失败则显示错误。 </span>

**`ZIPARCHIVE::FL_NOCASE`** (<span class="type">integer</span>)  
<span class="simpara"> 查找时忽略名称的大小写。 </span>

**`ZIPARCHIVE::FL_NODIR`** (<span class="type">integer</span>)  
<span class="simpara"> 忽略目录部分 </span>

**`ZIPARCHIVE::FL_COMPRESSED`** (<span class="type">integer</span>)  
<span class="simpara"> 读取压缩数据 </span>

**`ZIPARCHIVE::FL_UNCHANGED`** (<span class="type">integer</span>)  
<span class="simpara"> 使用原始数据，忽略更改。 </span>

**`ZipArchive::FL_RECOMPRESS`** (<span class="type">integer</span>)  
<span class="simpara"> 强制重新压缩数据。 PHP 8.0.0 和 PECL zip 1.18.0
起可以使用。 </span>

**`ZipArchive::FL_ENCRYPTED`** (<span class="type">integer</span>)  
<span class="simpara"> Read encrypted data (implies FL\_COMPRESSED).
Available as of PHP 8.0.0 and PECL zip 1.18.0. </span>

**`ZipArchive::FL_OVERWRITE`** (<span class="type">integer</span>)  
<span class="simpara"> If file with name exists, overwrite (replace) it.
Available as of PHP 8.0.0 and PECL zip 1.18.0. </span>

**`ZipArchive::FL_LOCAL`** (<span class="type">integer</span>)  
<span class="simpara"> In local header. Available as of PHP 8.0.0 and
PECL zip 1.18.0. </span>

**`ZipArchive::ZIP_FL_CENTRAL`** (<span class="type">integer</span>)  
<span class="simpara"> In central directory. Available as of PHP 8.0.0
and PECL zip 1.18.0. </span>

**`ZipArchive::FL_ENC_GUESS`** (<span class="type">integer</span>)  
<span class="simpara"> Guess string encoding (is default). Available as
of PHP 7.0.8. </span>

**`ZipArchive::FL_ENC_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> Get unmodified string. Available as of PHP 7.0.8.
</span>

**`ZipArchive::FL_ENC_STRICT`** (<span class="type">integer</span>)  
<span class="simpara"> Follow specification strictly. Available as of
PHP 7.0.8. </span>

**`ZipArchive::FL_ENC_UTF_8`** (<span class="type">integer</span>)  
<span class="simpara"> String is UTF-8 encoded. Available as of PHP
7.0.8. </span>

**`ZipArchive::FL_ENC_CP437`** (<span class="type">integer</span>)  
<span class="simpara"> String is CP437 encoded. Available as of PHP
7.0.8. </span>

**`ZIPARCHIVE::CM_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> 更好的压缩或存储。 </span>

**`ZIPARCHIVE::CM_STORE`** (<span class="type">integer</span>)  
<span class="simpara"> 存储（不压缩）。 </span>

**`ZIPARCHIVE::CM_SHRINK`** (<span class="type">integer</span>)  
<span class="simpara"> 收缩 </span>

**`ZIPARCHIVE::CM_REDUCE_1`** (<span class="type">integer</span>)  
<span class="simpara"> 用因子1换算 </span>

**`ZIPARCHIVE::CM_REDUCE_2`** (<span class="type">integer</span>)  
<span class="simpara"> 用因子2换算 </span>

**`ZIPARCHIVE::CM_REDUCE_3`** (<span class="type">integer</span>)  
<span class="simpara"> 用因子3换算 </span>

**`ZIPARCHIVE::CM_REDUCE_4`** (<span class="type">integer</span>)  
<span class="simpara"> 用因子4换算 </span>

**`ZIPARCHIVE::CM_IMPLODE`** (<span class="type">integer</span>)  
<span class="simpara"> 聚爆 </span>

**`ZIPARCHIVE::CM_DEFLATE`** (<span class="type">integer</span>)  
<span class="simpara"> deflated </span>

**`ZIPARCHIVE::CM_DEFLATE64`** (<span class="type">integer</span>)  
<span class="simpara"> deflate64 </span>

**`ZIPARCHIVE::CM_PKWARE_IMPLODE`** (<span class="type">integer</span>)  
<span class="simpara"> PKWARE imploding </span>

**`ZIPARCHIVE::CM_BZIP2`** (<span class="type">integer</span>)  
<span class="simpara"> BZIP2算法 </span>

**`ZipArchive::CM_LZMA`** (<span class="type">integer</span>)  
<span class="simpara"> LZMA 算法 </span>

**`ZipArchive::CM_LZMA2`** (<span class="type">integer</span>)  
<span class="simpara"> LZMA2 algorithm. Available as of PHP 7.4.3 and
PECL zip 1.16.0, respectively, if built against libzip ≥ 1.6.0. </span>

**`ZipArchive::CM_XZ`** (<span class="type">integer</span>)  
<span class="simpara"> XZ algorithm. Available as of PHP 7.4.3 and PECL
zip 1.16.1, respectively, if built against libzip ≥ 1.6.0. </span>

**`ZIPARCHIVE::ER_OK`** (<span class="type">integer</span>)  
<span class="simpara"> 没有错误。 </span>

**`ZIPARCHIVE::ER_MULTIDISK`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持多磁盘zip压缩包。 </span>

**`ZIPARCHIVE::ER_RENAME`** (<span class="type">integer</span>)  
<span class="simpara"> 重命名临时文件失败。 </span>

**`ZIPARCHIVE::ER_CLOSE`** (<span class="type">integer</span>)  
<span class="simpara"> 关闭zip压缩包失败。 </span>

**`ZIPARCHIVE::ER_SEEK`** (<span class="type">integer</span>)  
<span class="simpara"> 寻址错误 </span>

**`ZIPARCHIVE::ER_READ`** (<span class="type">integer</span>)  
<span class="simpara"> 读取错误 </span>

**`ZIPARCHIVE::ER_WRITE`** (<span class="type">integer</span>)  
<span class="simpara"> 写入错误 </span>

**`ZIPARCHIVE::ER_CRC`** (<span class="type">integer</span>)  
<span class="simpara"> CRC校验失败 </span>

**`ZIPARCHIVE::ER_ZIPCLOSED`** (<span class="type">integer</span>)  
<span class="simpara"> zip压缩包已关闭 </span>

**`ZIPARCHIVE::ER_NOENT`** (<span class="type">integer</span>)  
<span class="simpara"> 没有文件 </span>

**`ZIPARCHIVE::ER_EXISTS`** (<span class="type">integer</span>)  
<span class="simpara"> 文件已经存在 </span>

**`ZIPARCHIVE::ER_OPEN`** (<span class="type">integer</span>)  
<span class="simpara"> 不能打开文件 </span>

**`ZIPARCHIVE::ER_TMPOPEN`** (<span class="type">integer</span>)  
<span class="simpara"> 创建临时文件失败 </span>

**`ZIPARCHIVE::ER_ZLIB`** (<span class="type">integer</span>)  
<span class="simpara"> Zlib错误 </span>

**`ZIPARCHIVE::ER_MEMORY`** (<span class="type">integer</span>)  
<span class="simpara"> 内存分配失败 </span>

**`ZIPARCHIVE::ER_CHANGED`** (<span class="type">string</span>)  
<span class="simpara"> 条目已被改变 </span>

**`ZIPARCHIVE::ER_COMPNOTSUPP`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持的压缩方式 </span>

**`ZIPARCHIVE::ER_EOF`** (<span class="type">integer</span>)  
<span class="simpara"> 过早的EOF </span>

**`ZIPARCHIVE::ER_INVAL`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的参数 </span>

**`ZIPARCHIVE::ER_NOZIP`** (<span class="type">integer</span>)  
<span class="simpara"> 不是一个zip压缩包 </span>

**`ZIPARCHIVE::ER_INTERNAL`** (<span class="type">integer</span>)  
<span class="simpara"> 内部错误（Internal error） </span>

**`ZIPARCHIVE::ER_INCONS`** (<span class="type">integer</span>)  
<span class="simpara"> Zip压缩包不一致 </span>

**`ZIPARCHIVE::ER_REMOVE`** (<span class="type">integer</span>)  
<span class="simpara"> 不能移除文件 </span>

**`ZIPARCHIVE::ER_DELETED`** (<span class="type">integer</span>)  
<span class="simpara"> 条目已被删除 </span>

**`ZipArchive::ER_ENCRNOTSUPP`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持的压缩方式。 PHP 7.4.3 和 PECL zip 1.16.1
起可用。 </span>

**`ZipArchive::ER_RDONLY`** (<span class="type">integer</span>)  
<span class="simpara"> Read-only archive. Available as of PHP 7.4.3 and
PECL zip 1.16.1, respectively. </span>

**`ZipArchive::ER_NOPASSWD`** (<span class="type">integer</span>)  
<span class="simpara"> No password provided. Available as of PHP 7.4.3
and PECL zip 1.16.1, respectively. </span>

**`ZipArchive::ER_WRONGPASSWD`** (<span class="type">integer</span>)  
<span class="simpara"> Wrong password provided. Available as of PHP
7.4.3 and PECL zip 1.16.1, respectively. </span>

**`ZipArchive::ZIP_ER_OPNOTSUPP`** (<span class="type">integer</span>)  
<span class="simpara"> Operation not supported. Available as of PHP
7.4.3 and PECL zip 1.16.1, respectively, if built against libzip ≥
1.0.0. </span>

**`ZipArchive::ZIP_ER_INUSE`** (<span class="type">integer</span>)  
<span class="simpara"> Resource still in use. Available as of PHP 7.4.3
and PECL zip 1.16.1, respectively, if built against libzip ≥ 1.0.0.
</span>

**`ZipArchive::ZIP_ER_TELL`** (<span class="type">integer</span>)  
<span class="simpara"> Tell error. Available as of PHP 7.4.3 and PECL
zip 1.16.1, respectively, if built against libzip ≥ 1.0.0. </span>

**`ZipArchive::ZIP_ER_COMPRESSED_DATA`** (<span class="type">integer</span>)  
<span class="simpara"> Compressed data invalid. Available as of PHP
7.4.3 and PECL zip 1.16.1, respectively, if built against libzip ≥
1.6.0. </span>

**`ZipArchive::ER_CANCELLED`** (<span class="type">integer</span>)  
<span class="simpara"> Operation cancelled. Available as of PHP 7.4.3
and PECL zip 1.16.1, respectively, if built against libzip ≥ 1.6.0.
</span>

**`ZipArchive::EM_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> No encryption, since PHP 7.2.0, PECL zip 1.14.0
</span>

**`ZipArchive::EM_AES_128`** (<span class="type">integer</span>)  
<span class="simpara"> AES 128 encryption, since PHP 7.2.0, PECL zip
1.14.0 </span>

**`ZipArchive::EM_AES_192`** (<span class="type">integer</span>)  
<span class="simpara"> AES 1192 encryption, since PHP 7.2.0, PECL zip
1.14.0 </span>

**`ZipArchive::EM_AES_256`** (<span class="type">integer</span>)  
<span class="simpara"> AES 256 encryption, since PHP 7.2.0, PECL zip
1.14.0 </span>

**`ZipArchive::LIBZIP_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> Zip library version. Available as of PHP 7.4.3
and PECL zip 1.16.0. </span>

<!-- -->

**`ZipArchive::OPSYS_DOS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_AMIGA`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_OPENVMS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_UNIX`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_VM_CMS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_ATARI_ST`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_OS_2`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_MACINTOSH`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_Z_SYSTEM`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_CPM`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_WINDOWS_NTFS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_MVS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_VSE`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_ACORN_RISC`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_VFAT`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_ALTERNATE_MVS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_BEOS`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_TANDEM`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_OS_400`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_OS_X`** (<span class="type">integer</span>)  
**`ZipArchive::OPSYS_DEFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> Since PHP 5.6.0, PECL zip 1.12.4 </span>
