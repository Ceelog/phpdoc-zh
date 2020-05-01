转换过滤器
----------

如同 string.\* 过滤器，convert.\*
过滤器的作用就和其名字一样。转换过滤器是 PHP 5.0.0
添加的。对于指定过滤器的更多信息，请参考该函数的手册页。

*convert.base64-encode*和
*convert.base64-decode*使用这两个过滤器等同于分别用 <span
class="function">base64\_encode</span>和 <span
class="function">base64\_decode</span>函数处理所有的流数据。
*convert.base64-encode*支持以一个关联数组给出的参数。如果给出了
`line-length`，base64 输出将被用 `line-length`个字符为
长度而截成块。如果给出了
`line-break-chars`，每块将被用给出的字符隔开。这些参数的效果和用 <span
class="function">base64\_encode</span>再加上 <span
class="function">chunk\_split</span>相同。

**示例 \#1 convert.base64-encode & convert.base64-decode**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-encode');
fwrite($fp, "This is a test.\n");
fclose($fp);
/* Outputs:  VGhpcyBpcyBhIHRlc3QuCg==  */

$param = array('line-length' => 8, 'line-break-chars' => "\r\n");
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-encode', STREAM_FILTER_WRITE, $param);
fwrite($fp, "This is a test.\n");
fclose($fp);
/* Outputs:  VGhpcyBp
          :  cyBhIHRl
          :  c3QuCg==  */

$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.base64-decode');
fwrite($fp, "VGhpcyBpcyBhIHRlc3QuCg==");
fclose($fp);
/* Outputs:  This is a test.  */
?>
```

*convert.quoted-printable-encode*和
*convert.quoted-printable-decode*使用此过滤器的 decode 版本等同于用
<span
class="function">quoted\_printable\_decode</span>函数处理所有的流数据。没有和
*convert.quoted-printable-encode*相对应的函数。
*convert.quoted-printable-encode*支持以一个关联数组给出的参数。除了支持和
*convert.base64-encode*一样的附加参数外，
*convert.quoted-printable-encode*还支持布尔参数 `binary`和
`force-encode-first`。 *convert.base64-decode*只支持
`line-break-chars`参数作为从编码载荷中剥离的类型提示。

**示例 \#2 convert.quoted-printable-encode &
convert.quoted-printable-decode**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'convert.quoted-printable-encode');
fwrite($fp, "This is a test.\n");
/* Outputs:  =This is a test.=0A  */
?>
```
