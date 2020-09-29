JavaScript对象符号（JSON）
==========================

**目录**

-   [简介](/intro/json.html)
-   [安装／配置](/json/setup.html)
    -   [需求](/json/setup.html#需求)
    -   [安装](/json/setup.html#安装)
    -   [运行时配置](/json/setup.html#运行时配置)
    -   [资源类型](/json/setup.html#资源类型)
-   [预定义常量](/json/constants.html)
-   [JsonException](/class/jsonexception.html) — The JsonException class
-   [JsonSerializable](/class/jsonserializable.html) — JSON 序列化接口
    -   [JsonSerializable::jsonSerialize](/class/jsonserializable.html#JsonSerializable::jsonSerialize)
        — 指定需要被序列化成 JSON 的数据
-   [JSON 函数](/ref/json.html)
    -   [json\_decode](/ref/json.html#json_decode) — 对 JSON
        格式的字符串进行解码
    -   [json\_encode](/ref/json.html#json_encode) — 对变量进行 JSON
        编码
    -   [json\_last\_error\_msg](/ref/json.html#json_last_error_msg) —
        Returns the error string of the last json\_encode() or
        json\_decode() call
    -   [json\_last\_error](/ref/json.html#json_last_error) —
        返回最后发生的错误

简介
----

Exception thrown if **`JSON_THROW_ON_ERROR`** option is set for <span
class="function">json\_encode</span> or <span
class="function">json\_decode</span>. `code` contains the error type,
for possible values see <span class="function">json\_last\_error</span>.

类摘要
------

**JsonException**

<span class="ooclass"> class **JsonException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

实现 <span class="interfacename">JsonSerializable</span> 的类可以 在
<span class="function">json\_encode</span> 时定制他们的 JSON 表示法。

接口摘要
--------

**JsonSerializable**

<span class="ooclass"> class **JsonSerializable** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">jsonSerialize</span> ( <span
class="methodparam">void</span> )

}

JsonSerializable::jsonSerialize
===============================

指定需要被序列化成 JSON 的数据

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">JsonSerializable::jsonSerialize</span> ( <span
class="methodparam">void</span> )

序列化物体（Object）成能被 <span class="function">json\_encode</span>
原生地序列化的值。

### 参数

此函数没有参数。

### 返回值

返回能被 <span class="function">json\_encode</span> 序列化的数据，
这个值可以是除了 <span class="type">resource</span> 外的任意类型。

### 范例

**示例 \#1 <span
class="methodname">JsonSerializable::jsonSerialize</span> 例子 returning
an <span class="type">array</span>**

``` php
<?php
class ArrayValue implements JsonSerializable {
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize() {
        return $this->array;
    }
}

$array = [1, 2, 3];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

以上例程会输出：

    [
        1,
        2,
        3
    ]

**示例 \#2 <span
class="methodname">JsonSerializable::jsonSerialize</span> 例子
返回了一个关联数组 <span class="type">array</span>**

``` php
<?php
class ArrayValue implements JsonSerializable {
    public function __construct(array $array) {
        $this->array = $array;
    }

    public function jsonSerialize() {
        return $this->array;
    }
}

$array = ['foo' => 'bar', 'quux' => 'baz'];
echo json_encode(new ArrayValue($array), JSON_PRETTY_PRINT);
?>
```

以上例程会输出：

    {
        "foo": "bar",
        "quux": "baz"
    }

**示例 \#3 <span
class="methodname">JsonSerializable::jsonSerialize</span> 例子 返回一个
<span class="type">integer</span>**

``` php
<?php
class IntegerValue implements JsonSerializable {
    public function __construct($number) {
        $this->number = (integer) $number;
    }

    public function jsonSerialize() {
        return $this->number;
    }
}

echo json_encode(new IntegerValue(1), JSON_PRETTY_PRINT);
?>
```

以上例程会输出：

    1

**示例 \#4 <span
class="methodname">JsonSerializable::jsonSerialize</span> 例子 返回一个
<span class="type">string</span>**

``` php
<?php
class StringValue implements JsonSerializable {
    public function __construct($string) {
        $this->string = (string) $string;
    }

    public function jsonSerialize() {
        return $this->string;
    }
}

echo json_encode(new StringValue('Hello!'), JSON_PRETTY_PRINT);
?>
```

以上例程会输出：

    "Hello!"
