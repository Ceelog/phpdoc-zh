不向后兼容的变更
----------------

### PHP 核心中不向后兼容的变更

#### 以数组形式访问非数组

尝试以数组方式访问 <span class="type">null</span>，<span
class="type">bool</span>， <span class="type">int</span>，<span
class="type">float</span> 或 <span class="type">resource</span> （例如
*$null\["key"\]*）将会抛出 notice 通知。

#### <span class="function">get\_declared\_classes</span> 函数

<span class="function">get\_declared\_classes</span>
函数将不再返回匿名的类，假如它们没有被实例化的话。

#### *fn* 关键词

*fn*
成为了保留关键词。需要特别注意，它不能再做为函数名或类名使用，但是仍然可以做为方法名和常量名存在。

#### 文件尾部的 *\<?php* 标签

文件尾部的 *\<?php* 标签（不包含空行）将会被解释成一个 PHP
头标签。Previously it was interpreted either as a short opening tag
followed by literal *php* and resulted in a syntax error (with
*short\_open\_tag=1*) or was interpreted as a literal *\<?php* string
(with *short\_open\_tag=0*).

#### Stream wrappers

When using include/require on a stream, <span
class="methodname">streamWrapper::stream\_set\_option</span> will be
invoked with the **`STREAM_OPTION_READ_BUFFER`** option. Custom stream
wrapper implementations may need to implement the <span
class="methodname">streamWrapper::stream\_set\_option</span> method to
avoid a warning (always returning **`FALSE`** is a sufficient
implementation).

#### Serialization 序列化

序列化类型 *o* 被移除。因为它不是由 PHP
生成的，这可能会影响到之前项目中手动生成的序列化字符串。

#### 密码算法常量

密码哈希算法标识符现在是可空字符串，而不再是整数。

-   <span class="simpara"> **`PASSWORD_DEFAULT`** 之前是 int 1; 现在是
    **`NULL`** </span>
-   <span class="simpara"> **`PASSWORD_BCRYPT`** 之前是 int 1; 现在是
    string '2y' </span>
-   <span class="simpara"> **`PASSWORD_ARGON2I`** 之前是 int 2; 现在是
    string 'argon2i' </span>
-   <span class="simpara"> **`PASSWORD_ARGON2ID`** 之前是 int 3; 现在是
    string 'argon2id' </span>

应用中如果正常使用了常量
PASSWORD\_DEFAULT，PASSWORD\_BCRYPT，PASSWORD\_ARGON2I 和
PASSWORD\_ARGON2ID 将不会受到影响。

#### <span class="function">htmlentities</span> 函数

<span class="function">htmlentities</span> will now raise a notice
(instead of a strict standards warning) if it is used with an encoding
for which only basic entity substitution is supported, in which case it
is equivalent to <span class="function">htmlspecialchars</span>.

#### <span class="function">fread</span> and <span class="function">fwrite</span> 函数

<span class="function">fread</span> 和 <span
class="function">fwrite</span> 在操作失败的时候会返回
**`FALSE`**。之前的版本中会返回空字符串或 0。EAGAIN/EWOULDBLOCK
不视为故障。

这些函数现在也会在失败时发出 NOTICE
通知，例如当试图写入一个只读文件资源时。

### BCMath Arbitrary Precision Mathematics

BCMath functions will now warn if a non well-formed number is passed,
such as *"32foo"*. The argument will be interpreted as zero, as before.

### CURL

Attempting to serialize a <span class="classname">CURLFile</span> class
will now generate an exception. Previously the exception was only thrown
on unserialization.

Using **`CURLPIPE_HTTP1`** is deprecated, and is no longer supported as
of cURL 7.62.0.

The *$version* parameter of <span class="function">curl\_version</span>
is deprecated. If any value not equal to the default
**`CURLVERSION_NOW`** is passed, a warning is raised and the parameter
is ignored.

### Date and Time

Calling <span class="function">var\_dump</span> or similar on a <span
class="classname">DateTime</span> or <span
class="classname">DateTimeImmutable</span> instance will no longer leave
behind accessible properties on the object.

Comparison of <span class="classname">DateInterval</span> objects (using
*==*, *\<*, and so on) will now generate a warning and always return
**`FALSE`**. Previously all <span class="classname">DateInterval</span>
objects were considered equal, unless they had properties.

### Intl

The default parameter value of <span
class="function">idn\_to\_ascii</span> and <span
class="function">idn\_to\_utf8</span> is now
**`INTL_IDNA_VARIANT_UTS46`** instead of the deprecated
**`INTL_IDNA_VARIANT_2003`**.

### MySQLi

The embedded server functionality has been removed. It was broken since
at least PHP 7.0.

The undocumented *mysqli::$stat* property has been removed in favor of
<span class="methodname">mysqli::stat</span>.

### OpenSSL

The <span class="function">openssl\_random\_pseudo\_bytes</span>
function will now throw an exception in error situations, similar to
<span class="function">random\_bytes</span>. In particular, an <span
class="classname">Error</span> is thrown if the number of requested
bytes is less than or equal to zero, and an <span
class="classname">Exception</span> is thrown if sufficient randomness
cannot be gathered. The *$crypto\_strong output* argument is guaranteed
to always be **`TRUE`** if the function does not throw, so explicitly
checking it is not necessary.

### Regular Expressions (Perl-Compatible)

When **`PREG_UNMATCHED_AS_NULL`** mode is used, trailing unmatched
capturing groups will now also be set to **`NULL`** (or *\[null, -1\]*
if offset capture is enabled). This means that the size of the
*$matches* will always be the same.

### PHP Data Objects

Attempting to serialize a <span class="classname">PDO</span> or <span
class="classname">PDOStatement</span> instance will now generate an
<span class="classname">Exception</span> rather than a <span
class="classname">PDOException</span>, consistent with other internal
classes which do not support serialization.

### Reflection

Reflection objects will now generate an exception if an attempt is made
to serialize them. Serialization for reflection objects was never
supported and resulted in corrupted reflection objects. It has been
explicitly prohibited now.

### Standard PHP Library (SPL)

Calling <span class="function">get\_object\_vars</span> on an <span
class="classname">ArrayObject</span> instance will now always return the
properties of the <span class="classname">ArrayObject</span> itself (or
a subclass). Previously it returned the values of the wrapped
array/object unless the **`ArrayObject::STD_PROP_LIST`** flag was
specified.

Other affected operations are:

-   <span class="simpara"> <span
    class="methodname">ReflectionObject::getProperties</span> </span>
-   <span class="simpara"> <span class="function">reset</span>, <span
    class="function">current</span>, etc. Use <span
    class="interfacename">Iterator</span> methods instead. </span>
-   <span class="simpara"> Potentially others working on object
    properties as a list. </span>

*(array)* casts are not affected. They will continue to return either
the wrapped array, or the <span class="classname">ArrayObject</span>
properties, depending on whether the **`ArrayObject::STD_PROP_LIST`**
flag is used.

<span class="methodname">SplPriorityQueue::setExtractFlags</span> will
throw an exception if zero is passed. Previously this would generate a
recoverable fatal error on the next extraction operation.

<span class="classname">ArrayObject</span>, <span
class="classname">ArrayIterator</span>, <span
class="classname">SplDoublyLinkedList</span> and <span
class="classname">SplObjectStorage</span> now support the
*\_\_serialize()* and *\_\_unserialize()* mechanism in addition to the
<span class="interfacename">Serializable</span> interface. This means
that serialization payloads created on older PHP versions can still be
unserialized, but new payloads created by PHP 7.4 will not be understood
by older versions.

### Tokenizer

<span class="function">token\_get\_all</span> will now emit a
**`T_BAD_CHARACTER`** token for unexpected characters instead of leaving
behind holes in the token stream.

### 接收到的 Cookies

从 PHP 7.4.11 开始，为了安全考虑，接受到的 Cookie 中的 *names*
参数不再被 URL 编码。
