PHP 并不仅限于创建 HTML 输出， 它也可以创建和处理包括 GIF， PNG， JPEG，
WBMP 以及 XPM 在内的多种格式的图像。 更加方便的是，PHP
可以直接将图像数据流输出到浏览器。 要想在 PHP
中使用图像处理功能，你需要连带 GD 库一起来编译 PHP。 GD 库和 PHP
可能需要其他的库， 这取决于你要处理的图像格式。

你可以使用 PHP 中的图像函数来获取下列格式图像的大小： JPEG， GIF， PNG，
SWF， TIFF 和 JPEG2000。

如果联合 <a href="/ref/exif.html" class="link">exif 扩展</a> 一起使用，
你可以操作存储在 JPEG 和 TIFF 图像文件头部的信息，
这样就就可以获取数码相机所产生的元数据。 exif 相关的函数不需要 GD
库亦可使用。

> **Note**: <span class="simpara">
> 关于如何扩展图像处理能力，例如读取、写入以及修改， 请参考“需求”一节。
> 要想读取数码相机拍摄的图片的元数据， 你需要上面提到的
> <a href="/ref/exif.html" class="link">exif 扩展</a>。 </span>

> **Note**: <span class="simpara"> <span
> class="function">getimagesize</span> 函数不需要 GD 扩展库。 </span>

**Caution**

由于绑定的 GD 库使用 Zend 内存管理机制来分配内存，
所以所使用的内存大小不受
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
配置参数限制。

GD 库支持多种图像格式， 下标所列的是 GD
所支持的格式，请注意备图像格式对应的读取/写入支持的可用性。

| 格式 | 支持读取   | 支持写入    | 备注                                            |
|------|------------|-------------|-------------------------------------------------|
| JPEG | **`true`** | **`true`**  |                                                 |
| PNG  | **`true`** | **`true`**  |                                                 |
| GIF  | **`true`** | **`true`**  | 从 GD 2.0.28 及 PHP 5.0.1 开始支持              |
| XBM  | **`true`** | **`true`**  |                                                 |
| XPM  | **`true`** | **`false`** | 在 Windows 平台上，从 PHP 5.3.19 开始支持读取。 |
| WBMP | **`true`** | **`true`**  |                                                 |
| WebP | **`true`** | **`true`**  | PHP 5.5+                                        |
| BMP  | **`true`** | **`true`**  | 从 GD 2.1.0 及 PHP 7.2.0 开始支持               |

很遗憾的是，虽然上表中显示大部分图像格式都是支持读取和写入的，
但是不代表你的 PHP 环境在编译的时候是支持这些操作的。 要想检测 GD
库所支持的格式，请使用 <span class="function">gd\_info</span> 函数，
更多信息请参考 “安装” 一章。
