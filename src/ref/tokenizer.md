token\_get\_all
===============

将提供的源码按 PHP 标记进行分割

### 说明

<span class="type">array</span> <span
class="methodname">token\_get\_all</span> ( <span
class="methodparam"><span class="type">string</span> `$source`</span> )

<span class="function">token\_get\_all</span> 解析提供的 `source`
源码字符，然后使用 Zend 引擎的语法分析器获取源码中的 PHP
语言的解析器代号

解析器代号列表见<a href="/tokens.html" class="xref">解析器代号列表</a>,
或者使用 <span class="function">token\_name</span>
翻译获取这个代号的字符串表示.

### 参数

`source`  
需要解析的 PHP 源码.

### 返回值

An array of token identifiers. Each individual token identifier is
either a single character (i.e.: *;*, *.*, or a three element array
containing the token index in element 0, the string content of the
original token in element 1 and the line number in element 2.

### 范例

**示例 \#1 <span class="function">token\_get\_all</span> examples**

``` php
<?php
$tokens = token_get_all('<?php echo; ?>'); /* => array(
                                                  array(T_OPEN_TAG, '<?php'), 
                                                  array(T_ECHO, 'echo'),
                                                  ';',
                                                  array(T_CLOSE_TAG, '?>') ); */

/* Note in the following example that the string is parsed as T_INLINE_HTML
   rather than the otherwise expected T_COMMENT (T_ML_COMMENT in PHP <5).
   This is because no open/close tags were used in the "code" provided.
   This would be equivalent to putting a comment outside of <?php ?> tags in a normal file. */
$tokens = token_get_all('/* comment */'); // => array(array(T_INLINE_HTML, '/* comment */'));
?>
```

### 更新日志

| 版本  | 说明                                   |
|-------|----------------------------------------|
| 5.2.2 | Line numbers are returned in element 2 |

token\_name
===========

获取提供的 PHP 解析器代号的符号名称

### 说明

<span class="type">string</span> <span
class="methodname">token\_name</span> ( <span class="methodparam"><span
class="type">int</span> `$token`</span> )

<span class="function">token\_name</span> 获取一个 PHP `token`
的符号名称.

### 参数

`token`  
解析器代号的值.

### 返回值

提供的`token` 的符号名.

### 范例

**示例 \#1 <span class="function">token\_name</span> example**

``` php
<?php
// 260 is the token value for the T_EVAL token
echo token_name(260);        // -> "T_EVAL"

// a token constant maps to its own name
echo token_name(T_FUNCTION); // -> "T_FUNCTION"
?>
```

### 参见

-   <a href="/tokens.html" class="link">List of Parser Tokens</a>

**目录**

-   [token\_get\_all](/ref/tokenizer.html#token_get_all) —
    将提供的源码按 PHP 标记进行分割
-   [token\_name](/ref/tokenizer.html#token_name) — 获取提供的 PHP
    解析器代号的符号名称
