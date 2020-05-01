PHP 5.6.x 中已废止的特性
------------------------

### 从不兼容的上下文调用方法

现在已废止从不兼容的上下文调用方法， 并且产生 **`E_DEPRECATED`** 错误
（以前是 **`E_STRICT`**）。 在 PHP
的后续版本中可能彻底移除对此特性的支持。

以下是不兼容上下文调用方法的示例：

``` php
<?php
class A {
    function f() { echo get_class($this); }
}

class B {
    function f() { A::f(); }
}

(new B)->f();
?>
```

以上例程会输出：

    Deprecated: Non-static method A::f() should not be called statically, assuming $this from incompatible context in - on line 7
    B

### `$HTTP_RAW_POST_DATA` 和 <a href="/ini/core.html#ini.always-populate-raw-post-data" class="link">always_populate_raw_post_data</a>

使用
<a href="/ini/core.html#ini.always-populate-raw-post-data" class="link">always_populate_raw_post_data</a>
会导致在填充 `$HTTP_RAW_POST_DATA` 时产生 **`E_DEPRECATED`** 错误。
请使用
<a href="/wrappers/php.html#wrappers.php.input" class="link"><em>php://input</em></a>
替代 `$HTTP_RAW_POST_DATA`， 因为它可能在后续的 PHP 版本中被移除。 设置
<a href="/ini/core.html#ini.always-populate-raw-post-data" class="link">always_populate_raw_post_data</a>
为 *-1* （这样会强制 `$HTTP_RAW_POST_DATA` 未定义，所以也不回导致
**`E_DEPRECATED`** 的错误） 来体验新的行为。

### <a href="/book/iconv.html" class="link">iconv</a> 和 <a href="/book/mbstring.html" class="link">mbstring</a> 编码设置

<a href="/book/iconv.html" class="link">iconv</a> 和
<a href="/book/mbstring.html" class="link">mbstring</a> 配置选项中
和编码相关的选项都已废弃， 请使用
<a href="/ini/core.html#ini.default-charset" class="link"><code class="parameter">default_charset</code></a>。
废弃的选项有：

-   <span class="simpara">
    <a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.input_encoding</code></a>
    </span>
-   <span class="simpara">
    <a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.output_encoding</code></a>
    </span>
-   <span class="simpara">
    <a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.internal_encoding</code></a>
    </span>
-   <span class="simpara">
    <a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.http_input</code></a>
    </span>
-   <span class="simpara">
    <a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.http_output</code></a>
    </span>
-   <span class="simpara">
    <a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.internal_encoding</code></a>
    </span>
