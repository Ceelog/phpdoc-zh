不向后兼容的变更
----------------

尽管大部分现有的 PHP 5
代码不需要更改就可以正常运行，但请注意一些不向后兼容的变更：

### 不再支持 Windows XP 和 2003

已放弃对 Windows XP 和 2003 的支持。构建 Windows 版本的 PHP 需要 Windows
Vista 或更新的系统。

### Case insensitivity no longer locale specific

All case insensitive matching for function, class and constant names is
now performed in a locale independent manner according to ASCII rules.
This improves support for languages using the Latin alphabet with
unusual collating rules, such as Turkish and Azeri.

This may cause issues for code that uses case insensitive matches for
non-ASCII characters in multibyte character sets (including UTF-8), such
as accented characters in many European languages. If you have a
non-English, non-ASCII code base, then you will need to test that you
are not inadvertently relying on this behaviour before deploying PHP 5.5
to production systems.

### <span class="function">pack</span> 和 <span class="function">unpack</span> 函数的变化

为使 <span class="function">pack</span> 和 <span
class="function">unpack</span> 更兼容 Perl 做了一些变更：

-   <span class="simpara"> <span class="function">pack</span>
    现在支持“Z”格式代码，其表现的行为与“a”相同。 </span>
-   <span class="simpara"> <span class="function">unpack</span> now
    support the "Z" format code for NULL padded strings, and behaves as
    "a" did in previous versions: it will strip trailing NULL
    bytes.且其行为类似上一个版本中的“a”：清除后面的 NULL 字节。 </span>
-   <span class="simpara"> <span class="function">unpack</span> now
    keeps trailing NULL bytes when the "a" format code is used. </span>
-   <span class="simpara"> <span class="function">unpack</span> now
    strips all trailing ASCII whitespace when the "A" format code is
    used. </span>

Writing backward compatible code that uses the "a" format code with
<span class="function">unpack</span> requires the use of <span
class="function">version\_compare</span>, due to the backward
compatibility break.

例如：

``` php
<?php
// 以前的代码：
$data = unpack('a5', $packed);

// 新的代码：
if (version_compare(PHP_VERSION, '5.5.0-dev', '>=')) {
  $data = unpack('Z5', $packed);
} else {
  $data = unpack('a5', $packed);
}
?>
```

### 移除 PHP logo GUIDs

The GUIDs that previously resulted in PHP outputting various logos have
been removed. This includes the removal of the functions to return those
GUIDs. The removed functions are:

-   <span class="simpara"> <span class="function">php\_logo\_guid</span>
    </span>
-   <span class="simpara"> <span
    class="function">php\_egg\_logo\_guid</span> </span>
-   <span class="simpara"> <span
    class="function">php\_real\_logo\_guid</span> </span>
-   <span class="simpara"> <span
    class="function">zend\_logo\_guid</span> </span>

### Internal execution changes

Extension authors should note that the **zend\_execute()** function can
no longer be overridden, and that numerous changes have been made to the
*execute\_data* struct and related function and method handling opcodes.

Most extension authors are unlikely to be affected, but those writing
extensions that hook deeply into the Zend Engine should read
<a href="/migration55/internals.html" class="link">the notes on these changes</a>.
