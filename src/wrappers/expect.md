expect://
=========

处理交互式的流

### 说明

由 `expect://` 封装协议打开的数据流 PTY 通过提供了对进程 stdio、stdout
和 stderr 的访问。

> **Note**: **该封装协议默认未开启**  
> <span class="simpara"> 为了使用 `expect://` 封装器，你必须安装
> <a href="https://pecl.php.net/" class="link external">» PECL</a> 上的
> <a href="https://pecl.php.net/package/expect" class="link external">» Expect</a>
> 扩展。 </span>

`expect://` (PECL)

### 用法

-   <span class="simpara">`expect://command`</span>

### 可选项

| 属性                                                                       | 支持 |
|----------------------------------------------------------------------------|------|
| 受 <a href="/filesystem/setup.html#" class="link">allow_url_fopen</a> 影响 | No   |
| 允许读取                                                                   | Yes  |
| 允许写入                                                                   | Yes  |
| 允许添加                                                                   | Yes  |
| 允许同时读和写                                                             | No   |
| 支持 <span class="function">stat</span>                                    | No   |
| 支持 <span class="function">unlink</span>                                  | No   |
| 支持 <span class="function">rename</span>                                  | No   |
| 支持 <span class="function">mkdir</span>                                   | No   |
| 支持 <span class="function">rmdir</span>                                   | No   |

### 范例
