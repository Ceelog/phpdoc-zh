json\_decode
============

对 JSON 格式的字符串进行解码

### 说明

<span class="type">mixed</span> <span
class="methodname">json\_decode</span> ( <span class="methodparam"><span
class="type">string</span> `$json`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$assoc`<span
class="initializer"> = **`FALSE`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$depth`<span
class="initializer"> = 512</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \]\]\] )

接受一个 JSON 编码的字符串并且把它转换为 PHP 变量

### 参数

`json`  
待解码的 `json` <span class="type">string</span> 格式的字符串。

这个函数仅能处理 UTF-8 编码的数据。

> **Note**:
>
> PHP implements a superset of JSON as specified in the original
> <a href="http://www.faqs.org/rfcs/rfc7159" class="link external">» RFC 7159</a>.

`assoc`  
当该参数为 **`TRUE`** 时，将返回 <span class="type">array</span> 而非
<span class="type">object</span> 。

`depth`  
指定递归深度。

`options`  
由 **`JSON_BIGINT_AS_STRING`**, **`JSON_INVALID_UTF8_IGNORE`**,
**`JSON_INVALID_UTF8_SUBSTITUTE`**, **`JSON_OBJECT_AS_ARRAY`**,
**`JSON_THROW_ON_ERROR`** 组成的掩码。
这些常量的行为在<a href="/json/constants.html" class="link">JSON constants</a>页面有进一步描述。

### 返回值

通过恰当的 PHP 类型返回在 `json` 中编码的数据。值*true*, *false* 和
*null* 会相应地返回 **`TRUE`**, **`FALSE`** 和 **`NULL`**。 如果 `json`
无法被解码， 或者编码数据深度超过了递归限制的话，将会返回**`NULL`** 。

### 更新日志

| 版本  | 说明                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 7.3.0 | **`JSON_THROW_ON_ERROR`** `options` was added.                                                                                                |
| 7.2.0 | **`JSON_INVALID_UTF8_IGNORE`**, and **`JSON_INVALID_UTF8_SUBSTITUTE`** `options` were added.                                                  |
| 7.1.0 | An empty JSON key ("") can be encoded to the empty object property instead of using a key with value *\_empty\_*.                             |
| 7.0.0 | Rejected RFC 7159 incompatible number formats - top level (07, 0xff, .1, -.1) and all levels (\[1.\], \[1.e1\])                               |
| 7.0.0 | An empty PHP string or value that after casting to string is an empty string (*NULL*, *FALSE*) results in JSON syntax error.                  |
| 5.6.0 | Invalid non-lowercased variants of the *true*, *false* and *null* literals are no longer accepted as valid input, and will generate warnings. |
| 5.4.0 | **`JSON_BIGINT_AS_STRING`**, and **`JSON_OBJECT_AS_ARRAY`** `options` were added.                                                             |
| 5.4.0 | The `options` parameter was added.                                                                                                            |
| 5.3.0 | Added the optional `depth`. The default recursion depth was increased from 128 to 512                                                         |
| 5.2.3 | The nesting limit was increased from 20 to 128                                                                                                |
| 5.2.1 | Added support for JSON decoding of basic types.                                                                                               |

### 范例

**示例 \#1 <span class="function">json\_decode</span> 的例子**

``` php
<?php
$json = '{"a":1,"b":2,"c":3,"d":4,"e":5}';

var_dump(json_decode($json));
var_dump(json_decode($json, true));

?>
```

以上例程会输出：

    object(stdClass)#1 (5) {
        ["a"] => int(1)
        ["b"] => int(2)
        ["c"] => int(3)
        ["d"] => int(4)
        ["e"] => int(5)
    }

    array(5) {
        ["a"] => int(1)
        ["b"] => int(2)
        ["c"] => int(3)
        ["d"] => int(4)
        ["e"] => int(5)
    }

**示例 \#2 Accessing invalid object properties**

Accessing elements within an object that contain characters not
permitted under PHP's naming convention (e.g. the hyphen) can be
accomplished by encapsulating the element name within braces and the
apostrophe.

``` php
<?php

$json = '{"foo-bar": 12345}';

$obj = json_decode($json);
print $obj->{'foo-bar'}; // 12345

?>
```

**示例 \#3 common mistakes using <span
class="function">json\_decode</span>**

``` php
<?php

// the following strings are valid JavaScript but not valid JSON

// the name and value must be enclosed in double quotes
// single quotes are not valid 
$bad_json = "{ 'bar': 'baz' }";
json_decode($bad_json); // null

// the name must be enclosed in double quotes
$bad_json = '{ bar: "baz" }';
json_decode($bad_json); // null

// trailing commas are not allowed
$bad_json = '{ bar: "baz", }';
json_decode($bad_json); // null

?>
```

**示例 \#4 `depth` errors**

``` php
<?php
// Encode the data.
$json = json_encode(
    array(
        1 => array(
            'English' => array(
                'One',
                'January'
            ),
            'French' => array(
                'Une',
                'Janvier'
            )
        )
    )
);

// Define the errors.
$constants = get_defined_constants(true);
$json_errors = array();
foreach ($constants["json"] as $name => $value) {
    if (!strncmp($name, "JSON_ERROR_", 11)) {
        $json_errors[$value] = $name;
    }
}

// Show the errors for different depths.
foreach (range(4, 3, -1) as $depth) {
    var_dump(json_decode($json, true, $depth));
    echo 'Last error: ', $json_errors[json_last_error()], PHP_EOL, PHP_EOL;
}
?>
```

以上例程会输出：

    array(1) {
      [1]=>
      array(2) {
        ["English"]=>
        array(2) {
          [0]=>
          string(3) "One"
          [1]=>
          string(7) "January"
        }
        ["French"]=>
        array(2) {
          [0]=>
          string(3) "Une"
          [1]=>
          string(7) "Janvier"
        }
      }
    }
    Last error: JSON_ERROR_NONE

    NULL
    Last error: JSON_ERROR_DEPTH

**示例 \#5 <span class="function">json\_decode</span> of large
integers**

``` php
<?php
$json = '{"number": 12345678901234567890}';

var_dump(json_decode($json));
var_dump(json_decode($json, false, 512, JSON_BIGINT_AS_STRING));

?>
```

以上例程会输出：

    object(stdClass)#1 (1) {
      ["number"]=>
      float(1.2345678901235E+19)
    }
    object(stdClass)#1 (1) {
      ["number"]=>
      string(20) "12345678901234567890"
    }

### 注释

> **Note**:
>
> The JSON spec is not JavaScript, but a subset of JavaScript.

> **Note**:
>
> In the event of a failure to decode, <span
> class="function">json\_last\_error</span> can be used to determine the
> exact nature of the error.

### 参见

-   <span class="function">json\_encode</span>
-   <span class="function">json\_last\_error</span>

json\_encode
============

对变量进行 JSON 编码

### 说明

<span class="type">string</span> <span
class="methodname">json\_encode</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$options`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$depth`<span
class="initializer"> = 512</span></span> \]\] )

返回字符串，包含了 `value` 值 JSON 形式的表示。

编码受传入的 `options` 参数影响，此外浮点值的编码依赖于
<a href="/ini/core.html#ini.serialize-precision" class="link">serialize_precision</a>。

### 参数

`value`  
待编码的 `value` ，除了<span class="type">resource</span>
类型之外，可以为任何数据类型。

所有字符串数据的编码必须是 UTF-8。

> **Note**:
>
> PHP implements a superset of JSON as specified in the original
> <a href="http://www.faqs.org/rfcs/rfc7159" class="link external">» RFC 7159</a>.

`options`  
由以下常量组成的二进制掩码： **`JSON_HEX_QUOT`**, **`JSON_HEX_TAG`**,
**`JSON_HEX_AMP`**, **`JSON_HEX_APOS`**, **`JSON_NUMERIC_CHECK`**,
**`JSON_PRETTY_PRINT`**, **`JSON_UNESCAPED_SLASHES`**,
**`JSON_FORCE_OBJECT`**, **`JSON_PRESERVE_ZERO_FRACTION`**,
**`JSON_UNESCAPED_UNICODE`**, **`JSON_PARTIAL_OUTPUT_ON_ERROR`**。 关于
JSON
常量详情参考<a href="/json/constants.html" class="link">JSON 常量</a>页面。

`depth`  
设置最大深度。 必须大于0。

### 返回值

成功则返回 JSON 编码的 <span class="type">string</span> 或者在失败时返回
**`FALSE`** 。

### 更新日志

| 版本  | 说明                                                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 7.1.0 | 对 Double 的值进行编码时，使用 <a href="/ini/core.html#ini.serialize-precision" class="link">serialize_precision</a> 代替 <a href="/ini/core.html#ini.precision" class="link">precision</a>。 |
| 5.6.6 | `options` 参数增加常量： **`JSON_PRESERVE_ZERO_FRACTION`**                                                                                                                                    |
| 5.5.0 | 增加 `depth` 参数。                                                                                                                                                                           |
| 5.5.0 | 增加了 **`JSON_PARTIAL_OUTPUT_ON_ERROR`** 选项。                                                                                                                                              |
| 5.5.0 | 失败时返回的值从 *null* 字符串改成 **`FALSE`**。                                                                                                                                              |
| 5.4.0 | `options` 参数增加常量： **`JSON_PRETTY_PRINT`**, **`JSON_UNESCAPED_SLASHES`**, 和 **`JSON_UNESCAPED_UNICODE`**。                                                                             |
| 5.3.3 | `options` 参数增加常量：**`JSON_NUMERIC_CHECK`**。                                                                                                                                            |
| 5.3.0 | 增加 `options` 参数.                                                                                                                                                                          |

### 范例

**示例 \#1 <span class="function">json\_encode</span> 例子**

``` php
<?php
$arr = array ('a'=>1,'b'=>2,'c'=>3,'d'=>4,'e'=>5);

echo json_encode($arr);
?>
```

以上例程会输出：

    {"a":1,"b":2,"c":3,"d":4,"e":5}

**示例 \#2 <span class="function">json\_encode</span> 函数中 `options`
参数的用法**

``` php
<?php
$a = array('<foo>',"'bar'",'"baz"','&blong&', "\xc3\xa9");

echo "Normal: ",  json_encode($a), "\n";
echo "Tags: ",    json_encode($a, JSON_HEX_TAG), "\n";
echo "Apos: ",    json_encode($a, JSON_HEX_APOS), "\n";
echo "Quot: ",    json_encode($a, JSON_HEX_QUOT), "\n";
echo "Amp: ",     json_encode($a, JSON_HEX_AMP), "\n";
echo "Unicode: ", json_encode($a, JSON_UNESCAPED_UNICODE), "\n";
echo "All: ",     json_encode($a, JSON_HEX_TAG | JSON_HEX_APOS | JSON_HEX_QUOT | JSON_HEX_AMP | JSON_UNESCAPED_UNICODE), "\n\n";

$b = array();

echo "Empty array output as array: ", json_encode($b), "\n";
echo "Empty array output as object: ", json_encode($b, JSON_FORCE_OBJECT), "\n\n";

$c = array(array(1,2,3));

echo "Non-associative array output as array: ", json_encode($c), "\n";
echo "Non-associative array output as object: ", json_encode($c, JSON_FORCE_OBJECT), "\n\n";

$d = array('foo' => 'bar', 'baz' => 'long');

echo "Associative array always output as object: ", json_encode($d), "\n";
echo "Associative array always output as object: ", json_encode($d, JSON_FORCE_OBJECT), "\n\n";
?>
```

以上例程会输出：

    Normal: ["<foo>","'bar'","\"baz\"","&blong&","\u00e9"]
    Tags: ["\u003Cfoo\u003E","'bar'","\"baz\"","&blong&","\u00e9"]
    Apos: ["<foo>","\u0027bar\u0027","\"baz\"","&blong&","\u00e9"]
    Quot: ["<foo>","'bar'","\u0022baz\u0022","&blong&","\u00e9"]
    Amp: ["<foo>","'bar'","\"baz\"","\u0026blong\u0026","\u00e9"]
    Unicode: ["<foo>","'bar'","\"baz\"","&blong&","é"]
    All: ["\u003Cfoo\u003E","\u0027bar\u0027","\u0022baz\u0022","\u0026blong\u0026","é"]

    Empty array output as array: []
    Empty array output as object: {}

    Non-associative array output as array: [[1,2,3]]
    Non-associative array output as object: {"0":{"0":1,"1":2,"2":3}}

    Associative array always output as object: {"foo":"bar","baz":"long"}
    Associative array always output as object: {"foo":"bar","baz":"long"}

**示例 \#3 选项 JSON\_NUMERIC\_CHECK 例子**

``` php
<?php
echo "Strings representing numbers automatically turned into numbers".PHP_EOL;
$numbers = array('+123123', '-123123', '1.2e3', '0.00001');
var_dump(
 $numbers,
 json_encode($numbers, JSON_NUMERIC_CHECK)
);
echo "Strings containing improperly formatted numbers".PHP_EOL;
$strings = array('+a33123456789', 'a123');
var_dump(
 $strings,
 json_encode($strings, JSON_NUMERIC_CHECK)
);
?>
```

以上例程的输出类似于：

    Strings representing numbers automatically turned into numbers
    array(4) {
      [0]=>
      string(7) "+123123"
      [1]=>
      string(7) "-123123"
      [2]=>
      string(5) "1.2e3"
      [3]=>
      string(7) "0.00001"
    }
    string(28) "[123123,-123123,1200,1.0e-5]"
    Strings containing improperly formatted numbers
    array(2) {
      [0]=>
      string(13) "+a33123456789"
      [1]=>
      string(4) "a123"
    }
    string(24) "["+a33123456789","a123"]"

**示例 \#4 连续与非连续数组示例**

``` php
<?php
echo "连续数组".PHP_EOL;
$sequential = array("foo", "bar", "baz", "blong");
var_dump(
 $sequential,
 json_encode($sequential)
);

echo PHP_EOL."非连续数组".PHP_EOL;
$nonsequential = array(1=>"foo", 2=>"bar", 3=>"baz", 4=>"blong");
var_dump(
 $nonsequential,
 json_encode($nonsequential)
);

echo PHP_EOL."删除一个连续数组值的方式产生的非连续数组".PHP_EOL;
unset($sequential[1]);
var_dump(
 $sequential,
 json_encode($sequential)
);
?>
```

以上例程会输出：

    连续数组
    array(4) {
      [0]=>
      string(3) "foo"
      [1]=>
      string(3) "bar"
      [2]=>
      string(3) "baz"
      [3]=>
      string(5) "blong"
    }
    string(27) "["foo","bar","baz","blong"]"

    非连续数组
    array(4) {
      [1]=>
      string(3) "foo"
      [2]=>
      string(3) "bar"
      [3]=>
      string(3) "baz"
      [4]=>
      string(5) "blong"
    }
    string(43) "{"1":"foo","2":"bar","3":"baz","4":"blong"}"

    删除一个连续数组值的方式产生的非连续数组
    array(3) {
      [0]=>
      string(3) "foo"
      [2]=>
      string(3) "baz"
      [3]=>
      string(5) "blong"
    }
    string(33) "{"0":"foo","2":"baz","3":"blong"}"

**示例 \#5 **`选项 JSON_PRESERVE_ZERO_FRACTION`** 的例子**

``` php
<?php
var_dump(json_encode(12.0, JSON_PRESERVE_ZERO_FRACTION));
var_dump(json_encode(12.0));
?>
```

以上例程会输出：

    string(4) "12.0"
    string(2) "12"

### 注释

> **Note**:
>
> 如果执行失败，可以通过 <span class="function">json\_last\_error</span>
> 函数来获取详细错误信息。

> **Note**:
>
> 如果要编码的数组的键不是从0开始的数字，所有的键将会被当作字符串，并明确声明为
> key-value 对。

> **Note**:
>
> Like the reference JSON encoder, <span
> class="function">json\_encode</span> will generate JSON that is a
> simple value (that is, neither an object nor an array) if given a
> <span class="type">string</span>, <span class="type">integer</span>,
> <span class="type">float</span> or <span class="type">boolean</span>
> as an input `value`. While most decoders will accept these values as
> valid JSON, some may not, as the specification is ambiguous on this
> point.
>
> 总而言之，应该测试下 JSON decoder 能否处理 <span
> class="function">json\_encode</span> 生成的数据。

### 参见

-   <span class="interfacename">JsonSerializable</span>
-   <span class="function">json\_decode</span>
-   <span class="function">json\_last\_error</span>
-   <span class="function">serialize</span>

json\_last\_error\_msg
======================

Returns the error string of the last json\_encode() or json\_decode()
call

### 说明

<span class="type">string</span> <span
class="methodname">json\_last\_error\_msg</span> ( <span
class="methodparam">void</span> )

Returns the error string of the last <span
class="function">json\_encode</span> or <span
class="function">json\_decode</span> call, which did not specify
**`JSON_THROW_ON_ERROR`**.

### 参数

此函数没有参数。

### 返回值

Returns the error message on success, *"No error"* if no error has
occurred, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">json\_last\_error</span>

json\_last\_error
=================

返回最后发生的错误

### 说明

<span class="type">int</span> <span
class="methodname">json\_last\_error</span> ( <span
class="methodparam">void</span> )

如果有，返回 JSON 编码解码时最后发生的错误。

### 参数

此函数没有参数。

### 返回值

返回一个整型（integer），这个值会是以下的常量之一：

| 常量                                   | 含义                                                                                                                                                                                                                                                      | 可用性    |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **`JSON_ERROR_NONE`**                  | 没有错误发生                                                                                                                                                                                                                                              |           |
| **`JSON_ERROR_DEPTH`**                 | 到达了最大堆栈深度                                                                                                                                                                                                                                        |           |
| **`JSON_ERROR_STATE_MISMATCH`**        | 无效或异常的 JSON                                                                                                                                                                                                                                         |           |
| **`JSON_ERROR_CTRL_CHAR`**             | 控制字符错误，可能是编码不对                                                                                                                                                                                                                              |           |
| **`JSON_ERROR_SYNTAX`**                | 语法错误                                                                                                                                                                                                                                                  |           |
| **`JSON_ERROR_UTF8`**                  | 异常的 UTF-8 字符，也许是因为不正确的编码。                                                                                                                                                                                                               | PHP 5.3.3 |
| **`JSON_ERROR_RECURSION`**             | One or more recursive references in the value to be encoded                                                                                                                                                                                               | PHP 5.5.0 |
| **`JSON_ERROR_INF_OR_NAN`**            | One or more <a href="/language/types/float.html#language.types.float.nan" class="link"><strong><code>NAN</code></strong></a> or <a href="/ref/math.html#is_infinite" class="link"><strong><code>INF</code></strong></a> values in the value to be encoded | PHP 5.5.0 |
| **`JSON_ERROR_UNSUPPORTED_TYPE`**      | 指定的类型，值无法编码。                                                                                                                                                                                                                                  | PHP 5.5.0 |
| **`JSON_ERROR_INVALID_PROPERTY_NAME`** | 指定的属性名无法编码。                                                                                                                                                                                                                                    | PHP 7.0.0 |
| **`JSON_ERROR_UTF16`**                 | 畸形的 UTF-16 字符，可能因为字符编码不正确。                                                                                                                                                                                                              | PHP 7.0.0 |

### 范例

**示例 \#1 <span class="function">json\_last\_error</span> 例子**

``` php
<?php
// 一个有效的 json 字符串
$json[] = '{"Organization": "PHP Documentation Team"}';

// 一个无效的 json 字符串会导致一个语法错误，在这个例子里我们使用 ' 代替了 " 作为引号
$json[] = "{'Organization': 'PHP Documentation Team'}";


foreach ($json as $string) {
    echo 'Decoding: ' . $string;
    json_decode($string);

    switch (json_last_error()) {
        case JSON_ERROR_NONE:
            echo ' - No errors';
        break;
        case JSON_ERROR_DEPTH:
            echo ' - Maximum stack depth exceeded';
        break;
        case JSON_ERROR_STATE_MISMATCH:
            echo ' - Underflow or the modes mismatch';
        break;
        case JSON_ERROR_CTRL_CHAR:
            echo ' - Unexpected control character found';
        break;
        case JSON_ERROR_SYNTAX:
            echo ' - Syntax error, malformed JSON';
        break;
        case JSON_ERROR_UTF8:
            echo ' - Malformed UTF-8 characters, possibly incorrectly encoded';
        break;
        default:
            echo ' - Unknown error';
        break;
    }

    echo PHP_EOL;
}
?>
```

以上例程会输出：

    Decoding: {"Organization": "PHP Documentation Team"} - No errors
    Decoding: {'Organization': 'PHP Documentation Team'} - Syntax error, malformed JSON

**示例 \#2 <span class="function">json\_encode</span> 的 <span
class="function">json\_last\_error</span>**

``` php
<?php
// 无效的 UTF8 序列
$text = "\xB1\x31";

$json  = json_encode($text);
$error = json_last_error();

var_dump($json, $error === JSON_ERROR_UTF8);
?>
```

以上例程会输出：

    string(4) "null"
    bool(true)

### 参见

-   <span class="function">json\_last\_error\_msg</span>
-   <span class="function">json\_decode</span>
-   <span class="function">json\_encode</span>

**目录**

-   [json\_decode](/ref/json.html#json_decode) — 对 JSON
    格式的字符串进行解码
-   [json\_encode](/ref/json.html#json_encode) — 对变量进行 JSON 编码
-   [json\_last\_error\_msg](/ref/json.html#json_last_error_msg) —
    Returns the error string of the last json\_encode() or
    json\_decode() call
-   [json\_last\_error](/ref/json.html#json_last_error) —
    返回最后发生的错误
