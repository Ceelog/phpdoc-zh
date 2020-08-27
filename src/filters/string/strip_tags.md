string.strip\_tags
------------------

使用此过滤器等同于用 <span
class="function">strip\_tags</span>函数处理所有的流数据。可以用两种格式接收参数：一种是和
<span
class="function">strip\_tags</span>函数第二个参数相似的一个包含有标记列表的字符串，一种是一个包含有标记名的数组。

**Warning**

本特性已自 PHP 7.3.0 起*废弃*。强烈建议不要使用本特性。

**示例 \#1 string.strip\_tags**

``` php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.strip_tags', STREAM_FILTER_WRITE, "<b><i><u>");
fwrite($fp, "<b>bolded text</b> enlarged to a <h1>level 1 heading</h1>\n");
fclose($fp);
/* Outputs:  <b>bolded text</b> enlarged to a level 1 heading   */

$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.strip_tags', STREAM_FILTER_WRITE, array('b','i','u'));
fwrite($fp, "<b>bolded text</b> enlarged to a <h1>level 1 heading</h1>\n");
fclose($fp);
/* Outputs:  <b>bolded text</b> enlarged to a level 1 heading   */
?>
```
