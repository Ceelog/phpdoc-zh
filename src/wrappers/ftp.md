ftp://
======

ftps://
=======

访问 FTP(s) URLs

### 说明

允许通过 FTP 读取存在的文件，以及创建新文件。
如果服务器不支持被动（passive）模式的 FTP，连接会失败。

打开文件后你既可以读也可以写，但是不能同时进行。 当远程文件已经存在于
ftp 服务器上，如果尝试打开并写入文件的时候， 未指定上下文（context）选项
*overwrite*，连接会失败。 如果要通过 FTP 覆盖存在的文件，
指定上下文（context）的 *overwrite* 选项来打开、写入。 另外可使用
<a href="/ref/ftp.html" class="link">FTP 扩展</a>来代替。

如果你设置了 `php.ini` 中的
<a href="/filesystem/setup.html#" class="link">from</a> 指令，
这个值会作为匿名（anonymous）ftp 的密码。

### 用法

-   <span class="simpara">`ftp://example.com/pub/file.txt`</span>
-   <span
    class="simpara">`ftp://user:password@example.com/pub/file.txt`</span>
-   <span class="simpara">`ftps://example.com/pub/file.txt`</span>
-   <span
    class="simpara">`ftps://user:password@example.com/pub/file.txt`</span>

### 可选项

| 属性                                                                       | 是否支持                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 受 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> 影响 | 是                                                                                                                                                                                                                                                                              |
| 允许读取                                                                   | 是                                                                                                                                                                                                                                                                              |
| 允许写入                                                                   | 是 (新文件/启用 `overwrite` 后已存在的文件)                                                                                                                                                                                                                                     |
| 允许添加                                                                   | 是                                                                                                                                                                                                                                                                              |
| 允许同时读和写                                                             | 否                                                                                                                                                                                                                                                                              |
| 支持 <span class="function">stat</span>                                    | 仅 <span class="function">filesize</span>、 <span class="function">filetype</span>、 <span class="function">file\_exists</span>、 <span class="function">is\_file</span> 和 <span class="function">is\_dir</span>。 自 PHP 5.1.0 起： <span class="function">filemtime</span>。 |
| 支持 <span class="function">unlink</span>                                  | 是                                                                                                                                                                                                                                                                              |
| 支持 <span class="function">rename</span>                                  | 是                                                                                                                                                                                                                                                                              |
| 支持 <span class="function">mkdir</span>                                   | 是                                                                                                                                                                                                                                                                              |
| 支持 <span class="function">rmdir</span>                                   | 是                                                                                                                                                                                                                                                                              |

### 注释

> **Note**:
>
> FTPS 仅在 <a href="/book/openssl.html" class="link">openssl</a>
> 扩展开启时有效。
>
> <span class="simpara"> 如果服务器不支持 SSL，这个连接会降级（falls
> back）到普通未加密的 ftp。 </span>

> **Note**: **追加**  
> <span class="simpara"> 文件可以通过 *ftp://* URL
> 封装器来追加（append）。 </span>

### 参见

-   <a href="/context/ftp.html" class="xref">FTP context options</a>
