预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

以下常量表示了 <span class="function">json\_last\_error</span> 函数，或
<span class="classname">JsonException</span> 类中的 `code`
变量所返回的错误类型。

**`JSON_ERROR_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> 没有错误发生。自 PHP 5.3.0 起生效。 </span>

**`JSON_ERROR_DEPTH`** (<span class="type">integer</span>)  
<span class="simpara"> 到达了最大堆栈深度。自 PHP 5.3.0 起生效。 </span>

**`JSON_ERROR_STATE_MISMATCH`** (<span class="type">integer</span>)  
<span class="simpara"> 出现了下溢（underflow）或者模式不匹配。自 PHP
5.3.0 起生效。 </span>

**`JSON_ERROR_CTRL_CHAR`** (<span class="type">integer</span>)  
<span class="simpara"> 控制字符错误，可能是编码不对。自 PHP 5.3.0
起生效。 </span>

**`JSON_ERROR_SYNTAX`** (<span class="type">integer</span>)  
<span class="simpara"> 语法错误。自 PHP 5.3.0 起生效。 </span>

**`JSON_ERROR_UTF8`** (<span class="type">integer</span>)  
<span class="simpara"> 异常的 UTF-8 字符，也许是因为不正确的编码。自 PHP
5.3.3 起生效。 </span>

**`JSON_ERROR_RECURSION`** (<span class="type">integer</span>)  
<span class="simpara"> 传递给 <span class="function">json\_encode</span>
函数的对象或数组包含了递归引用，导致无法被编码。如果打开了
**`JSON_PARTIAL_OUTPUT_ON_ERROR`** 选项，则牵涉到递归引用的数据会转换成
**`NULL`** 后返回。自 PHP 5.5.0 起生效。 </span>

**`JSON_ERROR_INF_OR_NAN`** (<span class="type">integer</span>)  
<span class="simpara"> 传递给 <span class="function">json\_encode</span>
函数的参数中包含了
<a href="/language/types/float.html#language.types.float.nan" class="link"><strong><code>NAN</code></strong></a>
或
<a href="/ref/math.html#is_infinite" class="link"><strong><code>INF</code></strong></a>，导致编码出错。如果打开了
**`JSON_PARTIAL_OUTPUT_ON_ERROR`**
选项，则牵涉到对应不可编码的数字，会转换成数字 *0* 后返回。自 PHP 5.5.0
起生效。 </span>

**`JSON_ERROR_UNSUPPORTED_TYPE`** (<span class="type">integer</span>)  
<span class="simpara"> 传递了不支持的数据类型给 <span
class="function">json\_encode</span> 函数，比如
<a href="/language/types/resource.html" class="link">资源(resource)</a>。如果打开了
**`JSON_PARTIAL_OUTPUT_ON_ERROR`**
选项，则对于不支持的数据类型，会转换成 **`NULL`** 后返回。自 PHP 5.5.0
起生效。 </span>

**`JSON_ERROR_INVALID_PROPERTY_NAME`** (<span class="type">integer</span>)  
<span class="simpara"> A key starting with \\u0000 character was in the
string passed to <span class="function">json\_decode</span> when
decoding a JSON object into a PHP object. Available since PHP 7.0.0.
</span>

**`JSON_ERROR_UTF16`** (<span class="type">integer</span>)  
<span class="simpara"> Single unpaired UTF-16 surrogate in unicode
escape contained in the JSON string passed to <span
class="function">json\_encode</span>. Available since PHP 7.0.0. </span>

下面的常量可以和 <span class="function">json\_decode</span> 的 form
选项结合使用。

**`JSON_BIGINT_AS_STRING`** (<span class="type">integer</span>)  
<span class="simpara"> 将大数字编码成原始字符原来的值。 自 PHP 5.4.0
起生效。 </span>

**`JSON_OBJECT_AS_ARRAY`** (<span class="type">integer</span>)  
<span class="simpara"> Decodes JSON objects as PHP array. This option
can be added automatically by calling <span
class="function">json\_decode</span> with the second parameter equal to
**`TRUE`**. Available since PHP 5.4.0. </span>

下面的常量可以和 <span class="function">json\_encode</span> 的 form
选项结合使用。

**`JSON_HEX_TAG`** (<span class="type">integer</span>)  
<span class="simpara"> 所有的 \< 和 \> 转换成 \\u003C 和 \\u003E。 自
PHP 5.3.0 起生效。 </span>

**`JSON_HEX_AMP`** (<span class="type">integer</span>)  
<span class="simpara"> 所有的 & 转换成 \\u0026。 自 PHP 5.3.0 起生效。
</span>

**`JSON_HEX_APOS`** (<span class="type">integer</span>)  
<span class="simpara"> 所有的 ' 转换成 \\u0027。 自 PHP 5.3.0 起生效。
</span>

**`JSON_HEX_QUOT`** (<span class="type">integer</span>)  
<span class="simpara"> 所有的 " 转换成 \\u0022。 自 PHP 5.3.0 起生效。
</span>

**`JSON_FORCE_OBJECT`** (<span class="type">integer</span>)  
<span class="simpara"> 使一个非关联数组输出一个类（Object）而非数组。
在数组为空而接受者需要一个类（Object）的时候尤其有用。 自 PHP 5.3.0
起生效。 </span>

**`JSON_NUMERIC_CHECK`** (<span class="type">integer</span>)  
<span class="simpara"> 将所有数字字符串编码成数字（numbers）。 自 PHP
5.3.3 起生效。 </span>

**`JSON_PRETTY_PRINT`** (<span class="type">integer</span>)  
<span class="simpara"> 用空白字符格式化返回的数据。 自 PHP 5.4.0
起生效。 </span>

**`JSON_UNESCAPED_SLASHES`** (<span class="type">integer</span>)  
<span class="simpara"> 不要编码 */*。 自 PHP 5.4.0 起生效。 </span>

**`JSON_UNESCAPED_UNICODE`** (<span class="type">integer</span>)  
<span class="simpara"> 以字面编码多字节 Unicode 字符（默认是编码成
\\uXXXX）。 自 PHP 5.4.0 起生效。 </span>

**`JSON_PARTIAL_OUTPUT_ON_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Substitute some unencodable values instead of
failing. Available since PHP 5.5.0. </span>

**`JSON_PRESERVE_ZERO_FRACTION`** (<span class="type">integer</span>)  
<span class="simpara"> Ensures that <span class="type">float</span>
values are always encoded as a float value. Available since PHP 5.6.6.
</span>

**`JSON_UNESCAPED_LINE_TERMINATORS`** (<span class="type">integer</span>)  
<span class="simpara"> The line terminators are kept unescaped when
**`JSON_UNESCAPED_UNICODE`** is supplied. It uses the same behaviour as
it was before PHP 7.1 without this constant. Available since PHP 7.1.0.
</span>

下面的常量可以和 <span class="function">json\_decode</span> 及 <span
class="function">json\_encode</span> 的 form 选项结合使用。

**`JSON_INVALID_UTF8_IGNORE`** (<span class="type">integer</span>)  
<span class="simpara"> Ignore invalid UTF-8 characters. Available as of
PHP 7.2.0. </span>

**`JSON_INVALID_UTF8_SUBSTITUTE`** (<span class="type">integer</span>)  
<span class="simpara"> Convert invalid UTF-8 characters to \\0xfffd
(Unicode Character 'REPLACEMENT CHARACTER') Available as of PHP 7.2.0.
</span>

**`JSON_THROW_ON_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Throws <span
class="classname">JsonException</span> if an error occurs instead of
setting the global error state that is retrieved with <span
class="function">json\_last\_error</span> and <span
class="function">json\_last\_error\_msg</span>.
**`JSON_PARTIAL_OUTPUT_ON_ERROR`** takes precedence over
**`JSON_THROW_ON_ERROR`**. Available as of PHP 7.3.0. </span>
