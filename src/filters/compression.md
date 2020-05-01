压缩过滤器
----------

虽然
<a href="/wrappers/compression.html" class="link">压缩封装协议</a>提供了在本地文件系统中
创建 gzip 和 bz2
兼容文件的方法，但不代表可以在网络的流中提供通用压缩的意思，也不代表可以将一个非压缩的流转换成一个压缩流。对此，压缩过滤器可以在任何时候应用于任何流资源。

> **Note**: <span class="simpara">压缩过滤器 *不*产生命令行工具如
> *gzip*的头和尾信息。只是压缩和解压数据流中的有效载荷部分。</span>

*zlib.deflate*（压缩）和 *zlib.inflate*（解压）实现了定义与
<a href="http://www.faqs.org/rfcs/rfc1951" class="link external">» RFC 1951</a>的压缩算法。
*deflate*过滤器可以接受以一个关联数组传递的最多三个参数。
`level`定义了压缩强度（1-9）。数字更高通常会产生更小的载荷，但要消耗更多的处理时间。存在两个特殊压缩等级：0（完全不压缩）和
-1（zlib 内部默认值，目前是 6）。
`window`是压缩回溯窗口大小，以二的次方表示。更高的值（大到 15 —— 32768
字节）产生更好的压缩效果但消耗更多内存，低的值（低到 9 —— 512
字节）产生产生较差的压缩效果但内存消耗低。目前默认的 `window`大小是
**`15`**。 `memory`用来指示要分配多少工作内存。合法的数值范围是从
1（最小分配）到
9（最大分配）。内存分配仅影响速度，不会影响生成的载荷的大小。

> **Note**: <span
> class="simpara">因为最常用的参数是压缩等级，也可以提供一个整数值作为此参数（而不用数组）。</span>

zlib.\* 压缩过滤器自 PHP 版本 *5.1.0*起可用，在激活
<a href="/ref/zlib.html" class="link">zlib</a>的前提下。也可以通过安装来自
<a href="https://pecl.php.net/" class="link external">» PECL</a>的
<a href="https://pecl.php.net/package/zlib_filter" class="link external">» zlib_filter</a>包作为一个后门在
*5.0.x*版中使用。此过滤器在 PHP 4 中 *不可用*。

**示例 \#1 *zlib.deflate*和 *zlib.inflate***

``` php
<?php
$params = array('level' => 6, 'window' => 15, 'memory' => 9);

$original_text = "This is a test.\nThis is only a test.\nThis is not an important string.\n";
echo "The original text is " . strlen($original_text) . " characters long.\n";

$fp = fopen('test.deflated', 'w');
stream_filter_append($fp, 'zlib.deflate', STREAM_FILTER_WRITE, $params);
fwrite($fp, $original_text);
fclose($fp);

echo "The compressed file is " . filesize('test.deflated') . " bytes long.\n";
echo "The original text was:\n";
/* Use readfile and zlib.inflate to decompress on the fly */
readfile('php://filter/zlib.inflate/resource=test.deflated');

/* Generates output:

The original text is 70 characters long.
The compressed file is 56 bytes long.
The original text was:
This is a test.
This is only a test.
This is not an important string.

 */
?>
```

**示例 \#2 *zlib.deflate*简单参数用法**

``` php
<?php
$original_text = "This is a test.\nThis is only a test.\nThis is not an important string.\n";
echo "The original text is " . strlen($original_text) . " characters long.\n";

$fp = fopen('test.deflated', 'w');
/* Here "6" indicates compression level 6 */
stream_filter_append($fp, 'zlib.deflate', STREAM_FILTER_WRITE, 6);
fwrite($fp, $original_text);
fclose($fp);

echo "The compressed file is " . filesize('test.deflated') . " bytes long.\n";

/* Generates output:

The original text is 70 characters long.
The compressed file is 56 bytes long.

 */
?>
```

*bzip2.compress*和 *bzip2.decompress*工作的方式与上面讲的 zlib
过滤器相同。
*bzip2.compress*过滤器接受以一个关联数组给出的最多两个参数：
`blocks`是从 1 到 9 的整数值，指定分配多少个 100K
字节的内存块作为工作区。 `work`是 0 到 250
的整数值，指定在退回到一个慢一些，但更可靠的算法之前做多少次常规压缩算法的尝试。调整此参数仅影响到速度，压缩输出和内存使用都不受此设置的影响。将此参数设为
0 指示 bzip 库使用内部默认算法。
*bzip2.decompress*过滤器仅接受一个参数，可以用普通的布尔值传递，或者用一个关联数组中的
`small`单元传递。当 `small`设为 &true; 值时，指示 bzip
库用最小的内存占用来执行解压缩，代价是速度会慢一些。

bzip2.\* 压缩过滤器自 PHP 版本 *5.1.0*起可用，在激活
<a href="/ref/bzip2.html" class="link">bz2</a>支持的前提下。也可以通过安装来自
<a href="https://pecl.php.net/" class="link external">» PECL</a>的
<a href="https://pecl.php.net/package/bz2_filter" class="link external">» bz2_filter</a>包作为一个后门在
*5.0.x*版中使用。此过滤器在 PHP 4 中 *不可用*。

**示例 \#3 *bzip2.compress*和 *bzip2.decompress***

``` php
<?php
$param = array('blocks' => 9, 'work' => 0);

echo "The original file is " . filesize('LICENSE') . " bytes long.\n";

$fp = fopen('LICENSE.compressed', 'w');
stream_filter_append($fp, 'bzip2.compress', STREAM_FILTER_WRITE, $param);
fwrite($fp, file_get_contents('LICENSE'));
fclose($fp);

echo "The compressed file is " . filesize('LICENSE.compressed') . " bytes long.\n";

/* Generates output:

The original text is 3288 characters long.
The compressed file is 1488 bytes long.

 */
?>
```
