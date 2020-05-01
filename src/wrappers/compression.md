zlib://
=======

bzip2://
========

zip://
======

压缩流

### 说明

`compress.zlib://` and `compress.bzip2://`

`zlib:` 的功能类似 <span class="function">gzopen</span>，但是
其数据流还能被 <span class="function">fread</span>
和其他文件系统函数使用。 自 PHP 4.3.0
后这个不建议被使用，因为会和其他带“:”字符的文件名混淆； 请使用
`compress.zlib://` 作为替代。

`compress.zlib://`、 `compress.bzip2://` 和 <span
class="function">gzopen</span>、<span class="function">bzopen</span>
是相等的。并且可以在不支持 fopencookie 的系统中使用。

<a href="/book/zip.html" class="link">ZIP 扩展</a> 注册了 `zip:`
封装器。 自 PHP 7.2.0 和 libzip 1.2.0+
起，加密归档开始支持密码，允许数据流中使用密码。 字节流上下文（stream
contexts）中使用 *'password'* 选项设置密码。

### 可选项

-   <span class="simpara">`compress.zlib://file.gz`</span>
-   <span class="simpara">`compress.bzip2://file.bz2`</span>
-   <span class="simpara">`zip://archive.zip#dir/file.txt`</span>

### 用法

| 属性                                                                      | 支持                                            |
|---------------------------------------------------------------------------|-------------------------------------------------|
| 受限于 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> | No                                              |
| 允许读取                                                                  | Yes                                             |
| 允许写入                                                                  | Yes（除了 *zip://*）                            |
| 允许附加                                                                  | Yes（除了 *zip://*）                            |
| 允许同时读写                                                              | No                                              |
| 支持 <span class="function">stat</span>                                   | No，请使用普通的 *file://* 封装器统计压缩文件。 |
| 支持 <span class="function">unlink</span>                                 | No，请使用 *file://* 封装器删除压缩文件。       |
| 支持 <span class="function">rename</span>                                 | No                                              |
| 支持 <span class="function">mkdir</span>                                  | No                                              |
| 支持 <span class="function">rmdir</span>                                  | No                                              |
