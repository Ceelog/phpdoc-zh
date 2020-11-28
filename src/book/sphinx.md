Sphinx 客户端
=============

**目录**

-   [简介](/intro/sphinx.html)
-   [安装／配置](/sphinx/setup.html)
    -   [需求](/sphinx/setup.html#需求)
    -   [安装](/sphinx/setup.html#安装)
    -   [运行时配置](/sphinx/setup.html#运行时配置)
    -   [资源类型](/sphinx/setup.html#资源类型)
-   [预定义常量](/sphinx/constants.html)
-   [范例](/sphinx/examples.html)
-   [SphinxClient](/class/sphinxclient.html) — SphinxClient 类
    -   [SphinxClient::addQuery](/class/sphinxclient.html#SphinxClient::addQuery)
        — Add query to multi-query batch
    -   [SphinxClient::buildExcerpts](/class/sphinxclient.html#SphinxClient::buildExcerpts)
        — Build text snippets
    -   [SphinxClient::buildKeywords](/class/sphinxclient.html#SphinxClient::buildKeywords)
        — Extract keywords from query
    -   [SphinxClient::close](/class/sphinxclient.html#SphinxClient::close)
        — 关闭先前打开的持久连接
    -   [SphinxClient::\_\_construct](/class/sphinxclient.html#SphinxClient::__construct)
        — Create a new SphinxClient object
    -   [SphinxClient::escapeString](/class/sphinxclient.html#SphinxClient::escapeString)
        — Escape special characters
    -   [SphinxClient::getLastError](/class/sphinxclient.html#SphinxClient::getLastError)
        — Get the last error message
    -   [SphinxClient::getLastWarning](/class/sphinxclient.html#SphinxClient::getLastWarning)
        — Get the last warning
    -   [SphinxClient::open](/class/sphinxclient.html#SphinxClient::open)
        — 建立到搜索服务端的持久连接
    -   [SphinxClient::query](/class/sphinxclient.html#SphinxClient::query)
        — 执行搜索查询
    -   [SphinxClient::resetFilters](/class/sphinxclient.html#SphinxClient::resetFilters)
        — Clear all filters
    -   [SphinxClient::resetGroupBy](/class/sphinxclient.html#SphinxClient::resetGroupBy)
        — Clear all group-by settings
    -   [SphinxClient::runQueries](/class/sphinxclient.html#SphinxClient::runQueries)
        — Run a batch of search queries
    -   [SphinxClient::setArrayResult](/class/sphinxclient.html#SphinxClient::setArrayResult)
        — 控制搜索结果集的返回格式
    -   [SphinxClient::setConnectTimeout](/class/sphinxclient.html#SphinxClient::setConnectTimeout)
        — Set connection timeout
    -   [SphinxClient::setFieldWeights](/class/sphinxclient.html#SphinxClient::setFieldWeights)
        — Set field weights
    -   [SphinxClient::setFilter](/class/sphinxclient.html#SphinxClient::setFilter)
        — 增加整数值过滤器
    -   [SphinxClient::setFilterFloatRange](/class/sphinxclient.html#SphinxClient::setFilterFloatRange)
        — Add new float range filter
    -   [SphinxClient::setFilterRange](/class/sphinxclient.html#SphinxClient::setFilterRange)
        — Add new integer range filter
    -   [SphinxClient::setGeoAnchor](/class/sphinxclient.html#SphinxClient::setGeoAnchor)
        — Set anchor point for a geosphere distance calculations
    -   [SphinxClient::setGroupBy](/class/sphinxclient.html#SphinxClient::setGroupBy)
        — Set grouping attribute
    -   [SphinxClient::setGroupDistinct](/class/sphinxclient.html#SphinxClient::setGroupDistinct)
        — Set attribute name for per-group distinct values count
        calculations
    -   [SphinxClient::setIDRange](/class/sphinxclient.html#SphinxClient::setIDRange)
        — Set a range of accepted document IDs
    -   [SphinxClient::setIndexWeights](/class/sphinxclient.html#SphinxClient::setIndexWeights)
        — Set per-index weights
    -   [SphinxClient::setLimits](/class/sphinxclient.html#SphinxClient::setLimits)
        — 设置返回结果集偏移量和数目
    -   [SphinxClient::setMatchMode](/class/sphinxclient.html#SphinxClient::setMatchMode)
        — 设置全文查询的匹配模式
    -   [SphinxClient::setMaxQueryTime](/class/sphinxclient.html#SphinxClient::setMaxQueryTime)
        — Set maximum query time
    -   [SphinxClient::setOverride](/class/sphinxclient.html#SphinxClient::setOverride)
        — Sets temporary per-document attribute value overrides
    -   [SphinxClient::setRankingMode](/class/sphinxclient.html#SphinxClient::setRankingMode)
        — Set ranking mode
    -   [SphinxClient::setRetries](/class/sphinxclient.html#SphinxClient::setRetries)
        — Set retry count and delay
    -   [SphinxClient::setSelect](/class/sphinxclient.html#SphinxClient::setSelect)
        — Set select clause
    -   [SphinxClient::setServer](/class/sphinxclient.html#SphinxClient::setServer)
        — 设置searchd的主机名和TCP端口
    -   [SphinxClient::setSortMode](/class/sphinxclient.html#SphinxClient::setSortMode)
        — Set matches sorting mode
    -   [SphinxClient::status](/class/sphinxclient.html#SphinxClient::status)
        — Queries searchd status
    -   [SphinxClient::updateAttributes](/class/sphinxclient.html#SphinxClient::updateAttributes)
        — Update document attributes

简介
----

SphinxClient 为 Sphinx 提供了面向对象的接口.

类摘要
------

**SphinxClient**

<span class="ooclass"> class **SphinxClient** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">addQuery</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "\*"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$comment`<span
class="initializer"> = ""</span></span> \]\] )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">buildExcerpts</span> ( <span
class="methodparam"><span class="type">array</span> `$docs`</span> ,
<span class="methodparam"><span class="type">string</span>
`$index`</span> , <span class="methodparam"><span
class="type">string</span> `$words`</span> \[, <span
class="methodparam"><span class="type">array</span> `$opts`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">buildKeywords</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">string</span>
`$index`</span> , <span class="methodparam"><span
class="type">bool</span> `$hits`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">escapeString</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLastError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getLastWarning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">open</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">query</span> ( <span class="methodparam"><span
class="type">string</span> `$query`</span> \[, <span
class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "\*"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$comment`<span
class="initializer"> = ""</span></span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resetFilters</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">resetGroupBy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">runQueries</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setArrayResult</span> ( <span
class="methodparam"><span class="type">bool</span> `$array_result`<span
class="initializer"> = false</span></span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setConnectTimeout</span> ( <span
class="methodparam"><span class="type">float</span> `$timeout`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFieldWeights</span> ( <span
class="methodparam"><span class="type">array</span> `$weights`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFilter</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">array</span>
`$values`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$exclude`<span class="initializer"> =
false</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFilterFloatRange</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">float</span>
`$min`</span> , <span class="methodparam"><span
class="type">float</span> `$max`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$exclude`<span
class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setFilterRange</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$min`</span>
, <span class="methodparam"><span class="type">int</span> `$max`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$exclude`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setGeoAnchor</span> ( <span
class="methodparam"><span class="type">string</span> `$attrlat`</span> ,
<span class="methodparam"><span class="type">string</span>
`$attrlong`</span> , <span class="methodparam"><span
class="type">float</span> `$latitude`</span> , <span
class="methodparam"><span class="type">float</span> `$longitude`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setGroupBy</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$func`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$groupsort`<span class="initializer"> = "@group desc"</span></span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setGroupDistinct</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setIDRange</span> ( <span
class="methodparam"><span class="type">int</span> `$min`</span> , <span
class="methodparam"><span class="type">int</span> `$max`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setIndexWeights</span> ( <span
class="methodparam"><span class="type">array</span> `$weights`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setLimits</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$limit`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$max_matches`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cutoff`<span
class="initializer"> = 0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setMatchMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setMaxQueryTime</span> ( <span
class="methodparam"><span class="type">int</span> `$qtime`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOverride</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$type`</span>
, <span class="methodparam"><span class="type">array</span>
`$values`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setRankingMode</span> ( <span
class="methodparam"><span class="type">int</span> `$ranker`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setRetries</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> \[,
<span class="methodparam"><span class="type">int</span> `$delay`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSelect</span> ( <span
class="methodparam"><span class="type">string</span> `$clause`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setServer</span> ( <span
class="methodparam"><span class="type">string</span> `$server`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSortMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$sortby`</span> \] )

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">status</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">updateAttributes</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> ,
<span class="methodparam"><span class="type">array</span>
`$attributes`</span> , <span class="methodparam"><span
class="type">array</span> `$values`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$mva`<span
class="initializer"> = **`FALSE`**</span></span> \] )

}

SphinxClient::addQuery
======================

Add query to multi-query batch

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SphinxClient::addQuery</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "\*"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$comment`<span
class="initializer"> = ""</span></span> \]\] )

Adds query with the current settings to multi-query batch. This method
doesn't affect current settings (sorting, filtering, grouping etc.) in
any way.

### 参数

`query`  
Query string.

`index`  
An index name (or names).

`comment`  

### 返回值

Returns an index in an array of results that will be returned by
<a href="/class/sphinxclient.html#SphinxClient::runQueries" class="xref"></a>
call or false on error.

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::runQueries" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::query" class="xref"></a>

SphinxClient::buildExcerpts
===========================

Build text snippets

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">SphinxClient::buildExcerpts</span> ( <span
class="methodparam"><span class="type">array</span> `$docs`</span> ,
<span class="methodparam"><span class="type">string</span>
`$index`</span> , <span class="methodparam"><span
class="type">string</span> `$words`</span> \[, <span
class="methodparam"><span class="type">array</span> `$opts`</span> \] )

Connects to searchd, requests it to generate excerpts (snippets) from
the given documents, and returns the results.

### 参数

`docs`  
Array of strings with documents' contents.

`index`  
Index name.

`words`  
Keywords to highlight.

`opts`  
Associative array of additional highlighting options (see below).

| Option             | Description                                                                                                           |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| "before\_match"    | A string to insert before a keyword match. Default is "\<b\>".                                                        |
| "after\_match"     | A string to insert after a keyword match. Default is "\</b\>".                                                        |
| "chunk\_separator" | A string to insert between snippet chunks (passages). Default is " ... ".                                             |
| "limit"            | Maximum snippet size, in symbols (codepoints). Integer, default is 256.                                               |
| "around"           | How much words to pick around each matching keywords block. Integer, default is 5.                                    |
| "exact\_phrase"    | Whether to highlight exact query phrase matches only instead of individual keywords. Boolean, default is **`FALSE`**. |
| "single\_passage"  | Whether to extract single best passage only. Boolean, default is **`FALSE`**.                                         |

### 返回值

Returns array of snippets on success 或者在失败时返回 **`FALSE`**.

SphinxClient::buildKeywords
===========================

Extract keywords from query

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SphinxClient::buildKeywords</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> ,
<span class="methodparam"><span class="type">string</span>
`$index`</span> , <span class="methodparam"><span
class="type">bool</span> `$hits`</span> )

Extracts keywords from `query` using tokenizer settings for the given
`index`, optionally with per-keyword occurrence statistics.

### 参数

`query`  
A query to extract keywords from.

`index`  
An index to get tokenizing settings and keyword occurrence statistics
from.

`hits`  
A boolean flag to enable/disable keyword statistics generation.

### 返回值

Returns an array of associative arrays with per-keyword information.

SphinxClient::close
===================

关闭先前打开的持久连接

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::close</span> ( <span
class="methodparam">void</span> )

关闭先前打开的持久连接.

### 参数

此函数没有参数。

### 更新日志

| PECL/sphinx 版本 | 说明                                                                           |
|------------------|--------------------------------------------------------------------------------|
| 1.0.3            | 新增函数 SphinxClient::close(), 仅在编译时使用 libsphinxclient \>= 0.9.9 有效. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::open" class="xref"></a>

SphinxClient::\_\_construct
===========================

Create a new SphinxClient object

### 说明

<span class="modifier">public</span> <span
class="methodname">SphinxClient::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a new <span class="classname">SphinxClient</span> object.

### 参数

此函数没有参数。

SphinxClient::escapeString
==========================

Escape special characters

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SphinxClient::escapeString</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

Escapes characters that are treated as special operators by the query
language parser.

### 参数

`string`  
String to escape.

### 返回值

Returns escaped string.

SphinxClient::getLastError
==========================

Get the last error message

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SphinxClient::getLastError</span> ( <span
class="methodparam">void</span> )

Returns string with the last error message. If there were no errors
during the previous API call, empty string is returned. This method
doesn't reset the error message, so you can safely call it several
times.

### 参数

此函数没有参数。

### 返回值

Returns the last error message or an empty string if there were no
errors.

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::getLastWarning" class="xref"></a>

SphinxClient::getLastWarning
============================

Get the last warning

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SphinxClient::getLastWarning</span> ( <span
class="methodparam">void</span> )

Returns last warning message. If there were no warnings during the
previous API call, empty string is returned. This method doesn't reset
the warning, so you can safely call it several times.

### 参数

此函数没有参数。

### 返回值

Returns the last warning message or an empty string if there were no
warnings.

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::getLastError" class="xref"></a>

SphinxClient::open
==================

建立到搜索服务端的持久连接

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::open</span> ( <span
class="methodparam">void</span> )

建立到搜索服务端的持久连接.

### 参数

此函数没有参数。

### 更新日志

| PECL/sphinx 版本 | 说明                                                                          |
|------------------|-------------------------------------------------------------------------------|
| 1.0.3            | 新增函数 SphinxClient::open(), 仅在编译时使用 libsphinxclient \>= 0.9.9 有效. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::close" class="xref"></a>

SphinxClient::query
===================

执行搜索查询

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SphinxClient::query</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> \[,
<span class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "\*"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$comment`<span
class="initializer"> = ""</span></span> \]\] )

连接到searchd服务器，根据服务器的当前设置执行给定的查询，取得并返回结果集.

### 参数

`query`  
查询字符串.

`index`  
索引名称 (可以为多个，使用逗号分割，或者为“\*”表示全部索引).

`comment`  
发送到searchd的查询日志的注释内容

### 返回值

如果搜索成功, <span class="function">SphinxClient::query</span>
返回的结果集列表包含找到的全部匹配项中的一部分，以及与查询相关的统计数据.
结果集是哈希结构，包含如下键和值:

| 键             | 值说明                                                                                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "matches"      | 存储文档ID以及其对应的另一个包含文档权重和属性值的hash表                                                                                                     |
| "total"        | 此查询在服务器检索所得的匹配文档总数（即服务器端结果集的大小，且与相关设置有关）                                                                             |
| "total\_found" | （服务器上找到和处理了的）索引中匹配文档的总数                                                                                                               |
| "words"        | 将查询关键字（关键字已经过大小写转换，取词干和其他处理）映射到一个包含关于关键字的统计数据（“docs”——在多少文档中出现，“hits”——共出现了多少次）的小hash表上。 |
| "error"        | searchd报告的错误信息                                                                                                                                        |
| "warning"      | searchd报告的警告信息                                                                                                                                        |

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::runQueries" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::addQuery" class="xref"></a>

SphinxClient::resetFilters
==========================

Clear all filters

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SphinxClient::resetFilters</span> ( <span
class="methodparam">void</span> )

Clears all currently set filters. This call is normally required when
using multi-queries. You might want to set different filters for
different queries in the batch. To do that, you should call <span
class="function">SphinxClient::resetFilters</span> and add new filters
using the respective calls.

### 返回值

没有返回值。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::resetGroupBy" class="xref"></a>

SphinxClient::resetGroupBy
==========================

Clear all group-by settings

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SphinxClient::resetGroupBy</span> ( <span
class="methodparam">void</span> )

Clears all currently group-by settings, and disables group-by. This call
is normally required only when using multi-queries.

### 返回值

没有返回值。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::resetGroupBy" class="xref"></a>

SphinxClient::runQueries
========================

Run a batch of search queries

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">SphinxClient::runQueries</span> ( <span
class="methodparam">void</span> )

Connects to searchd, runs a batch of all queries added using
<a href="/class/sphinxclient.html#SphinxClient::addQuery" class="xref"></a>,
obtains and returns the result sets.

### 返回值

Returns **`FALSE`** on failure and array of result sets on success.

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::addQuery" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::query" class="xref"></a>

SphinxClient::setArrayResult
============================

控制搜索结果集的返回格式

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setArrayResult</span> ( <span
class="methodparam"><span class="type">bool</span> `$array_result`<span
class="initializer"> = false</span></span> )

控制搜索结果集的返回格式（匹配项按数组返回还是按hash返回）.

### 参数

`array_result`  
如果 `array_result` 设置为 **`FALSE`**, 匹配项以PHP
hash格式返回，文档ID为键，其他信息（权重、属性）为值。如果
`array_result` 设置为 **`TRUE`**,
匹配项以普通数组返回，包括匹配项的全部信息（含文档ID）.

### 返回值

总是返回 **`TRUE`**.

SphinxClient::setConnectTimeout
===============================

Set connection timeout

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setConnectTimeout</span> ( <span
class="methodparam"><span class="type">float</span> `$timeout`</span> )

Sets connection timeout (in seconds) for searchd connection.

### 参数

`timeout`  
Timeout in seconds.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setMaxQueryTime" class="xref"></a>

SphinxClient::setFieldWeights
=============================

Set field weights

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setFieldWeights</span> ( <span
class="methodparam"><span class="type">array</span> `$weights`</span> )

Binds per-field weights by name.

Match ranking can be affected by per-field weights. See
<a href="http://sphinxsearch.com/" class="link external">» Sphinx documentation</a>
for an explanation on how phrase proximity ranking is affected. This
call lets you specify non-default weights for full-text fields.

The weights must be positive 32-bit integers, so be careful not to hit
32-bit integer maximum. The final weight is a 32-bit integer too.
Default weight value is 1. Unknown field names are silently ignored.

### 参数

`weights`  
Associative array of field names and field weights.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setIndexWeights" class="xref"></a>

SphinxClient::setFilter
=======================

增加整数值过滤器

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setFilter</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">array</span>
`$values`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$exclude`<span class="initializer"> =
false</span></span> \] )

在已有的过滤器列表中添加新的过滤器.

### 参数

`attribute`  
属性名称.

`values`  
整数值数组.

`exclude`  
如果设置为 **`TRUE`**, 则匹配该过滤规则的文档会被排除在结果之外.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setFilterFloatRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setFilterRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::resetFilters" class="xref"></a>

SphinxClient::setFilterFloatRange
=================================

Add new float range filter

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setFilterFloatRange</span> (
<span class="methodparam"><span class="type">string</span>
`$attribute`</span> , <span class="methodparam"><span
class="type">float</span> `$min`</span> , <span
class="methodparam"><span class="type">float</span> `$max`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$exclude`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Adds new float range filter to the existing list of filters. Only those
documents which have `attribute` value stored in the index between `min`
and `max` (including values that are exactly equal to `min` or `max`)
will be matched (or rejected, if `exclude` is **`TRUE`**).

### 参数

`attribute`  
An attribute name.

`min`  
Minimum value.

`max`  
Maximum value.

`exclude`  
If set to **`TRUE`**, matching documents are excluded from the result
set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setFilterRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setFilter" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::resetFilters" class="xref"></a>

SphinxClient::setFilterRange
============================

Add new integer range filter

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setFilterRange</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$min`</span>
, <span class="methodparam"><span class="type">int</span> `$max`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$exclude`<span class="initializer"> = **`FALSE`**</span></span> \] )

Adds new integer range filter to the existing list of filters. Only
those documents which have `attribute` value stored in the index between
`min` and `max` (including values that are exactly equal to `min` or
`max`) will be matched (or rejected, if `exclude` is **`TRUE`**).

### 参数

`attribute`  
An attribute name.

`min`  
Minimum value.

`max`  
Maximum value.

`exclude`  
If set to **`TRUE`**, matching documents are excluded from the result
set.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setFilterFloatRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setFilter" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::resetFilters" class="xref"></a>

SphinxClient::setGeoAnchor
==========================

Set anchor point for a geosphere distance calculations

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setGeoAnchor</span> ( <span
class="methodparam"><span class="type">string</span> `$attrlat`</span> ,
<span class="methodparam"><span class="type">string</span>
`$attrlong`</span> , <span class="methodparam"><span
class="type">float</span> `$latitude`</span> , <span
class="methodparam"><span class="type">float</span> `$longitude`</span>
)

Sets anchor point for a geosphere distance (geodistance) calculations
and enables them.

Once an anchor point is set, you can use magic "@geodist" attribute name
in your filters and/or sorting expressions.

### 参数

`attrlat`  
Name of a latitude attribute.

`attrlong`  
Name of a longitude attribute.

`latitude`  
Anchor latitude in radians.

`longitude`  
Anchor longitude in radians.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setFilterFloatRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setFilterRange" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setFilter" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::resetFilters" class="xref"></a>

SphinxClient::setGroupBy
========================

Set grouping attribute

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setGroupBy</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$func`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$groupsort`<span class="initializer"> = "@group desc"</span></span> \]
)

Sets grouping attribute, function, and group sorting mode, and enables
grouping.

Grouping feature is very similar to GROUP BY clause in SQL. Results
produced by this function call are going to be the same as produced by
the following pseudo code: **SELECT ... GROUP BY $func($attribute) ORDER
BY $groupsort**.

### 参数

`attribute`  
A string containing group-by attribute name.

`func`  
Constant, which sets a function applied to the attribute value in order
to compute group-by key.

`groupsort`  
An optional clause controlling how the groups are sorted.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::resetGroupBy" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setSortMode" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setGroupDistinct" class="xref"></a>

SphinxClient::setGroupDistinct
==============================

Set attribute name for per-group distinct values count calculations

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setGroupDistinct</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
)

Sets attribute name for per-group distinct values count calculations.
Only available for grouping queries. For each group, all values of
`attribute` will be stored, then the amount of distinct values will be
calculated and returned to the client. This feature is similar to
COUNT(DISTINCT) clause in SQL.

### 参数

`attribute`  
A string containing group-by attribute name.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setSortMode" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setGroupBy" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::resetGroupBy" class="xref"></a>

SphinxClient::setIDRange
========================

Set a range of accepted document IDs

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setIDRange</span> ( <span
class="methodparam"><span class="type">int</span> `$min`</span> , <span
class="methodparam"><span class="type">int</span> `$max`</span> )

Sets an accepted range of document IDs. Default range is from 0 to 0,
i.e. no limit. Only those records that have document ID between `min`
and `max` (including IDs exactly equal to `min` or `max`) will be
matched.

### 参数

`min`  
Minimum ID value.

`max`  
Maximum ID value.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setIndexWeights
=============================

Set per-index weights

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setIndexWeights</span> ( <span
class="methodparam"><span class="type">array</span> `$weights`</span> )

Sets per-index weights and enables weighted summing of match weights
across different indexes.

### 参数

`weights`  
An associative array mapping string index names to integer weights.
Default is empty array, i.e. weighting summing is disabled.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setLimits
=======================

设置返回结果集偏移量和数目

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setLimits</span> ( <span
class="methodparam"><span class="type">int</span> `$offset`</span> ,
<span class="methodparam"><span class="type">int</span> `$limit`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$max_matches`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$cutoff`<span
class="initializer"> = 0</span></span> \]\] )

给服务器端结果集设置一个偏移量 `offset`
从那个偏移量起向客户端返回的匹配项数目限制(`limit`) .
并且可以在服务器端设定当前查询的结果集大小 (`max_matches`)
，另有一个阈值 (`cutoff`)，当找到的匹配项达到这个阀值时就停止搜索。

### 参数

`offset`  
结果集的偏移量.

`limit`  
返回的匹配项数目.

`max_matches`  
设置控制搜索过程中searchd在内存中所保持的匹配项数目.

`cutoff`  
该设置是为高级性能优化而提供的. 它告诉searchd 在找到并处理 `cutoff`
个匹配后就强制停止.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setMatchMode
==========================

设置全文查询的匹配模式

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setMatchMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> )

设置全文查询的匹配模式. `mode` 是以下列出的常量之一.

| Constant              | Description                                       |
|-----------------------|---------------------------------------------------|
| SPH\_MATCH\_ALL       | 匹配所有查询词（默认模式）.                       |
| SPH\_MATCH\_ANY       | 匹配查询词中的任意一个.                           |
| SPH\_MATCH\_PHRASE    | 将整个查询看作一个词组，要求按顺序完整匹配.       |
| SPH\_MATCH\_BOOLEAN   | 将查询看作一个布尔表达式.                         |
| SPH\_MATCH\_EXTENDED  | 将查询看作一个Sphinx内部查询语言的表达式.         |
| SPH\_MATCH\_FULLSCAN  | 使用完全扫描，忽略查询词汇.                       |
| SPH\_MATCH\_EXTENDED2 | 类似 **`SPH_MATCH_EXTENDED`** ，并支持评分和权重. |

### 参数

`mode`  
匹配模式.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setRankingMode" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setSortMode" class="xref"></a>

SphinxClient::setMaxQueryTime
=============================

Set maximum query time

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setMaxQueryTime</span> ( <span
class="methodparam"><span class="type">int</span> `$qtime`</span> )

Sets maximum search query time.

### 参数

`qtime`  
Maximum query time, in milliseconds. It must be a non-negative integer.
Default value is 0, i.e. no limit.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setOverride
=========================

Sets temporary per-document attribute value overrides

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setOverride</span> ( <span
class="methodparam"><span class="type">string</span> `$attribute`</span>
, <span class="methodparam"><span class="type">int</span> `$type`</span>
, <span class="methodparam"><span class="type">array</span>
`$values`</span> )

Sets temporary (per-query) per-document attribute value overrides.
Override feature lets you "temporary" update attribute values for some
documents within a single query, leaving all other queries unaffected.
This might be useful for personalized data

### 参数

`attribute`  
An attribute name.

`type`  
An attribute type. Only supports scalar attributes.

`values`  
Array of attribute values that maps document IDs to overridden attribute
values.

### 更新日志

| PECL/sphinx 版本  | 说明                                                                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
| PECL sphinx 1.0.3 | Added SphinxClient::setOverride(), available only if compiled with libsphinxclient \>= 0.9.9. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setRankingMode
============================

Set ranking mode

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setRankingMode</span> ( <span
class="methodparam"><span class="type">int</span> `$ranker`</span> )

Sets ranking mode. Only available in **`SPH_MATCH_EXTENDED2`** matching
mode.

| Constant                   | Description                                                                                                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPH\_RANK\_PROXIMITY\_BM25 | Default ranking mode which uses both proximity and BM25 ranking.                                                                                                                                       |
| SPH\_RANK\_BM25            | Statistical ranking mode which uses BM25 ranking only (similar to most of other full-text engines). This mode is faster, but may result in worse quality on queries which contain more than 1 keyword. |
| SPH\_RANK\_NONE            | Disables ranking. This mode is the fastest. It is essentially equivalent to boolean searching, a weight of 1 is assigned to all matches.                                                               |

### 参数

`ranker`  
Ranking mode.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setMatchMode" class="xref"></a>

SphinxClient::setRetries
========================

Set retry count and delay

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setRetries</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> \[,
<span class="methodparam"><span class="type">int</span> `$delay`<span
class="initializer"> = 0</span></span> \] )

Sets distributed retry count and delay.

On temporary failures searchd will attempt up to `count` retries per
agent. `delay` is the delay between the retries, in milliseconds.
Retries are disabled by default. Note that this call will not make the
API itself retry on temporary failure; it only tells searchd to do so.

### 参数

`count`  
Number of retries.

<!-- -->

`delay`  
Delay between retries, in milliseconds.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setSelect
=======================

Set select clause

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setSelect</span> ( <span
class="methodparam"><span class="type">string</span> `$clause`</span> )

Sets the select clause, listing specific attributes to fetch, and
expressions to compute and fetch.

### 参数

`clause`  
SQL-like clause.

### 更新日志

| PECL/sphinx 版本  | 说明                                                                                        |
|-------------------|---------------------------------------------------------------------------------------------|
| PECL sphinx 1.0.1 | Added SphinxClient::setSelect(), available only if compiled with libsphinxclient \>= 0.9.9. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setServer
=======================

设置searchd的主机名和TCP端口

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setServer</span> ( <span
class="methodparam"><span class="type">string</span> `$server`</span> ,
<span class="methodparam"><span class="type">int</span> `$port`</span> )

设置searchd的主机名和TCP端口。此后的所有请求都使用新的主机和端口设置。默认的主机和端口分别是“localhost”和3312.

### 参数

`server`  
IP 或者主机名.

`port`  
端口.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

SphinxClient::setSortMode
=========================

Set matches sorting mode

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SphinxClient::setSortMode</span> ( <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$sortby`</span> \] )

Sets matches sorting mode. See available modes below.

| Constant                  | Description                                                                                                      |
|---------------------------|------------------------------------------------------------------------------------------------------------------|
| SPH\_SORT\_RELEVANCE      | Sort by relevance in descending order (best matches first).                                                      |
| SPH\_SORT\_ATTR\_DESC     | Sort by an attribute in descending order (bigger attribute values first).                                        |
| SPH\_SORT\_ATTR\_ASC      | Sort by an attribute in ascending order (smaller attribute values first).                                        |
| SPH\_SORT\_TIME\_SEGMENTS | Sort by time segments (last hour/day/week/month) in descending order, and then by relevance in descending order. |
| SPH\_SORT\_EXTENDED       | Sort by SQL-like combination of columns in ASC/DESC order.                                                       |
| SPH\_SORT\_EXPR           | Sort by an arithmetic expression.                                                                                |

### 参数

`mode`  
Sorting mode.

`sortby`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <a href="/class/sphinxclient.html#SphinxClient::setMatchMode" class="xref"></a>
-   <a href="/class/sphinxclient.html#SphinxClient::setSortMode" class="xref"></a>

SphinxClient::status
====================

Queries searchd status

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">array</span><span class="type">false</span></span> <span
class="methodname">SphinxClient::status</span> ( <span
class="methodparam">void</span> )

Queries searchd status, and returns an array of status variable name and
value pairs.

### 参数

此函数没有参数。

### 更新日志

| PECL/sphinx 版本  | 说明                                                                                     |
|-------------------|------------------------------------------------------------------------------------------|
| PECL sphinx 1.0.3 | Added SphinxClient::status(), available only if compiled with libsphinxclient \>= 0.9.9. |

### 返回值

Returns an associative array of search server statistics
或者在失败时返回 **`FALSE`**.

SphinxClient::updateAttributes
==============================

Update document attributes

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">int</span><span class="type">false</span></span> <span
class="methodname">SphinxClient::updateAttributes</span> ( <span
class="methodparam"><span class="type">string</span> `$index`</span> ,
<span class="methodparam"><span class="type">array</span>
`$attributes`</span> , <span class="methodparam"><span
class="type">array</span> `$values`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$mva`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Instantly updates given attribute values in given documents.

### 参数

`index`  
Name of the index (or indexes) to be updated.

`attributes`  
Array of attribute names, listing attributes that are updated.

`values`  
Associative array containing document IDs as keys and array of attribute
values as values.

### 返回值

Returns number of actually updated documents (0 or more) on success, or
**`FALSE`** on failure.
