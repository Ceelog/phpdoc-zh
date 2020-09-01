**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担。

Bcompiler 由于以下若干原因而写成：

-   在一个专有的 PHP 应用程序里对整个脚本进行编码
-   在一个专有的 PHP 应用程序里对一些类或者函数进行编码
-   使生产环境中的 php-gtk 产品应用于桌面客户端，而无需 php.exe。
-   PHP 到 C 转换器的可行性研究

这些目标的第一个是通过使用函数 <span
class="function">bcompiler\_write\_header</span>、 <span
class="function">bcompiler\_write\_file</span> 和 <span
class="function">bcompiler\_write\_footer</span> 实现的。
字节码文件可以以未压缩的或简单的格式写入。 The bytecode files can be
written as either uncompressed or plain.
使用生成的字节码，你可以简单使用 include 或者 require 语句来包含。

这些目标的第二个可以使用 <span
class="function">bcompiler\_write\_header</span>、 <span
class="function">bcompiler\_write\_class</span>、 <span
class="function">bcompiler\_write\_footer</span>、 <span
class="function">bcompiler\_read</span> 和 <span
class="function">bcompiler\_load</span> 函数实现。
字节码文件可以以未压缩的或简单的格式写入。 <span
class="function">bcompiler\_load</span> 读取了一个 bzip
压缩过的字节码文件，体积往往是原始文件的 1/3。

为了创建可执行的文件，bcompiler 要使用一个修改过的 sapi
文件或者已经被编译为共享库的一个版本的 PHP。 在这个方案里，bcompiler
从可执行文件的末尾读取了压缩过的字节码。

在仅使用未压缩过的字节码时，bcompiler 能够提高约 30% 的性能。
但是请留意未压缩过的字节码可能比源码大5倍
使用字节码压缩可以节省您的磁盘空间，但解压需要比解析源码花费更多时间。
同时 bcompiler 没有对字节码做任何优化，这功能会在将来添加……

在代码保护方面，有把握地讲，不可能重新创建确切的原始代码，并且没有附加的源码注释。
它将有效得阻止了重建和修改一个类。但是它可以从 bcompile
过的字节码中取出数据
——所以不要把你私人密码或者其他任何类似东西放在里面。
