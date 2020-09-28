新参数
------

在 PHP 5.3 中一些函数新增了参数和选项:

PHP 核心:

-   <span class="simpara"> <span
    class="function">clearstatcache</span> - 新增 `clear_realpath_cache`
    和 `filename` 参数. </span>
-   <span class="simpara"> <span class="function">copy</span> -
    新增流环境参数 `context`。 </span>
-   <span class="simpara"> <span class="function">fgetcsv</span> - 新增
    `escape` 参数. </span>
-   <span class="simpara"> <span class="function">ini\_get\_all</span> -
    新增 `details` 参数. </span>
-   <span class="simpara"> <span class="function">nl2br</span> - 新增
    `is_xhtml` 参数. </span>
-   <span class="simpara"> <span
    class="function">parse\_ini\_file</span> - 新增 `scanner_mode` 参数.
    </span>
-   <span class="simpara"> <span class="function">round</span> - 新增
    `mode` 参数. </span>
-   <span class="simpara"> <span
    class="function">stream\_context\_create</span> - 新增 `params`
    参数. </span>
-   <span class="simpara"> <span class="function">strstr</span> 和 <span
    class="function">stristr</span> - 新增 `before_needle` 参数. </span>

<a href="/book/json.html" class="link">json</a>:

-   <span class="simpara"> <span class="function">json\_encode</span> -
    新增 `options` 参数. </span>
-   <span class="simpara"> <span class="function">json\_decode</span> -
    新增 `depth` 参数. </span>

<a href="/book/stream.html" class="link">流(Streams)</a>:

-   <span class="simpara"> <span class="function">stream\_select</span>,
    <span class="function">stream\_set\_blocking</span>, <span
    class="function">stream\_set\_timeout</span>，和 <span
    class="function">stream\_set\_write\_buffer</span>
    使用用户空间流包裹器. </span>

sybase\_ct:

-   <span class="simpara"> <span
    class="function">sybase\_connect</span> - 新增 `new` 参数. </span>

PHP 5.3.0 中的新方法参数:

PHP 核心:

-   <span class="simpara"> <span
    class="methodname">Exception::\_\_construct</span> - 新增 `previous`
    参数. </span>
