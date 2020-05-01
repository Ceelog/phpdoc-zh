solr\_get\_version
==================

返回当前Solr扩展的版本

### 说明

<span class="type">string</span> <span
class="methodname">solr\_get\_version</span> ( <span
class="methodparam">void</span> )

函数已字符串形式返回扩展的当前版本。

### 参数

此函数没有参数。

### 返回值

获取成功则返回版本号，否则返回 **`FALSE`** 。

### 错误／异常

此函数不抛出异常

### 范例

**示例 \#1 <span class="function">solr\_get\_version</span> example**

``` php
<?php

$solr_version = solr_get_version();

print $solr_version;

?>
```

以上例程的输出类似于：

    0.9.6

### 参见

-   <span class="function">SolrUtils::getSolrVersion</span>

**目录**

-   [solr\_get\_version](/ref/solr.html#solr_get_version) —
    返回当前Solr扩展的版本
