file://
=======

访问本地文件系统

### 说明

*文件系统* 是 PHP 使用的默认封装协议，展现了本地文件系统。
当指定了一个相对路径（不以/、\\、\\\\或 Windows
盘符开头的路径）提供的路径将基于当前的工作目录。
在很多情况下是脚本所在的目录，除非被修改了。 使用 CLI
的时候，目录默认是脚本被调用时所在的目录。

在某些函数里，例如 <span class="function">fopen</span> 和 <span
class="function">file\_get\_contents</span>， *include\_path*
会可选地搜索，也作为相对的路径。

### 用法

-   <span class="simpara">`/path/to/file.ext`</span>
-   <span class="simpara">`relative/path/to/file.ext`</span>
-   <span class="simpara">`fileInCwd.ext`</span>
-   <span class="simpara">`C:/path/to/winfile.ext`</span>
-   <span class="simpara">`C:\path\to\winfile.ext`</span>
-   <span class="simpara">`\\smbserver\share\path\to\winfile.ext`</span>
-   <span class="simpara">`file:///path/to/file.ext`</span>

### 可选项

| 属性                                                                       | 支持 |
|----------------------------------------------------------------------------|------|
| 受 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> 影响 | No   |
| 允许读取                                                                   | Yes  |
| 允许写入                                                                   | Yes  |
| 允许添加                                                                   | Yes  |
| 允许同时读和写                                                             | Yes  |
| 支持 <span class="function">stat</span>                                    | Yes  |
| 支持 <span class="function">unlink</span>                                  | Yes  |
| 支持 <span class="function">rename</span>                                  | Yes  |
| 支持 <span class="function">mkdir</span>                                   | Yes  |
| 支持 <span class="function">rmdir</span>                                   | Yes  |

### 更新日志

| 版本  | 说明              |
|-------|-------------------|
| 5.0.0 | 添加了 *file://*. |
