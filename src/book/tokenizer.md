Tokenizer
=========

**目录**

-   [简介](/intro/tokenizer.html)
-   [安装／配置](/tokenizer/setup.html)
    -   [需求](/tokenizer/setup.html#需求)
    -   [安装](/tokenizer/setup.html#安装)
    -   [运行时配置](/tokenizer/setup.html#运行时配置)
    -   [资源类型](/tokenizer/setup.html#资源类型)
-   [预定义常量](/tokenizer/constants.html)
-   [范例](/tokenizer/examples.html)
-   [PhpToken](/class/phptoken.html) — The PhpToken class
    -   [PhpToken::\_\_construct](/class/phptoken.html#PhpToken::__construct)
        — Returns a new PhpToken object
    -   [PhpToken::getTokenName](/class/phptoken.html#PhpToken::getTokenName)
        — Returns the name of the token.
    -   [PhpToken::is](/class/phptoken.html#PhpToken::is) — Tells
        whether the token is of given kind.
    -   [PhpToken::isIgnorable](/class/phptoken.html#PhpToken::isIgnorable)
        — Tells whether the token would be ignored by the PHP parser.
    -   [PhpToken::\_\_toString](/class/phptoken.html#PhpToken::__toString)
        — Returns the textual content of the token.
    -   [PhpToken::tokenize](/class/phptoken.html#PhpToken::tokenize) —
        Splits given source into PHP tokens, represented by PhpToken
        objects.
-   [Tokenizer 函数](/ref/tokenizer.html)
    -   [token\_get\_all](/ref/tokenizer.html#token_get_all) —
        将提供的源码按 PHP 标记进行分割
    -   [token\_name](/ref/tokenizer.html#token_name) — 获取提供的 PHP
        解析器代号的符号名称

简介
----

This class provides an alternative to <span
class="function">token\_get\_all</span>. While the function returns
tokens either as a single-character string, or an array with a token ID,
token text and line number, <span
class="function">PhpToken::tokenize</span> normalizes all tokens into
PhpToken objects, which makes code operating on tokens more memory
efficient and readable.

类摘要
------

**PhpToken**

<span class="ooclass"> class **PhpToken** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">int</span> `$id`
;

<span class="modifier">public</span> <span class="type">string</span>
`$text` ;

<span class="modifier">public</span> <span class="type">int</span>
`$line` ;

<span class="modifier">public</span> <span class="type">int</span>
`$pos` ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">int</span> `$line`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pos`<span
class="initializer"> = -1</span></span> \]\] )

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">getTokenName</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">is</span> ( <span class="methodparam"><span
class="type"><span class="type">int</span><span
class="type">string</span><span class="type">array</span></span>
`$kind`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isIgnorable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">tokenize</span> ( <span class="methodparam"><span
class="type">string</span> `$code`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

}

属性
----

`id`  
One of the T\_\* constants, or an ASCII codepoint representing a
single-char token.

`text`  
The textual content of the token.

`line`  
The starting line number (1-based) of the token.

`pos`  
The starting position (0-based) in the tokenized string.

PhpToken::\_\_construct
=======================

Returns a new PhpToken object

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">PhpToken::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$id`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> \[,
<span class="methodparam"><span class="type">int</span> `$line`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$pos`<span
class="initializer"> = -1</span></span> \]\] )

Returns a new PhpToken object

### 参数

`id`  
One of the T\_\* constants (see
<a href="/tokens.html" class="xref">解析器代号列表</a>), or an ASCII
codepoint representing a single-char token.

`text`  
The textual content of the token.

`line`  
The starting line number (1-based) of the token.

`pos`  
The starting position (0-based) in the tokenized string.

### 返回值

Returns a new PhpToken instance.

### 参见

-   <span class="function">PhpToken::tokenize</span>

PhpToken::getTokenName
======================

Returns the name of the token.

### 说明

<span class="modifier">public</span> <span class="type"><span
class="type">string</span><span class="type">null</span></span> <span
class="methodname">PhpToken::getTokenName</span> ( <span
class="methodparam">void</span> )

Returns the name of the token.

### 参数

此函数没有参数。

### 返回值

An ASCII character for single-char tokens, or one of T\_\* constant
names for known tokens (see
<a href="/tokens.html" class="xref">解析器代号列表</a>), or **`null`**
for unknown tokens.

### 范例

**示例 \#1 <span class="function">PhpToken::getTokenName</span>
example**

``` php
<?php
// known token
$token = new PhpToken(T_ECHO, 'echo');
var_dump($token->getTokenName());   // -> string(6) "T_ECHO"

// single-char token
$token = new PhpToken(ord(';'), ';');
var_dump($token->getTokenName());   // -> string(1) ";"

// unknown token
$token = new PhpToken(10000 , "\0");
var_dump($token->getTokenName());   // -> NULL
```

### 参见

-   <span class="function">PhpToken::tokenize</span>
-   <span class="function">token\_name</span>

PhpToken::is
============

Tells whether the token is of given kind.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PhpToken::is</span> ( <span
class="methodparam"><span class="type"><span
class="type">int</span><span class="type">string</span><span
class="type">array</span></span> `$kind`</span> )

Tells whether the token is of given `kind`.

### 参数

`kind`  
Either a single value to match the token's id or textual content, or an
array thereof.

### 返回值

A boolean value whether the token is of given kind.

### 范例

**示例 \#1 <span class="function">PhpToken::is</span> example**

``` php
<?php
$token = new PhpToken(T_ECHO, 'echo');
var_dump($token->is(T_ECHO));        // -> bool(true)
var_dump($token->is('echo'));        // -> bool(true)
var_dump($token->is(T_FOREACH));     // -> bool(false)
var_dump($token->is('foreach'));     // -> bool(false)
```

**示例 \#2 Usage with array**

``` php
<?php
function isClassType(PhpToken $token): bool {
    return $token->is([T_CLASS, T_INTERFACE, T_TRAIT]);
}

$interface = new PhpToken(T_INTERFACE, 'interface');
var_dump(isClassType($interface));   // -> bool(true)

$function = new PhpToken(T_FUNCTION, 'function');
var_dump(isClassType($function));    // -> bool(false)
```

### 参见

-   <span class="function">token\_name</span>

PhpToken::isIgnorable
=====================

Tells whether the token would be ignored by the PHP parser.

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PhpToken::isIgnorable</span> ( <span
class="methodparam">void</span> )

Tells whether the token would be ignored by the PHP parser.

### 参数

此函数没有参数。

### 返回值

A boolean value whether the token would be ignored by the PHP parser
(such as whitespace or comments).

### 范例

**示例 \#1 <span class="function">PhpToken::isIgnorable</span> example**

``` php
<?php
$echo = new PhpToken(T_ECHO, 'echo');
var_dump($echo->isIgnorable());   // -> bool(false)

$space = new PhpToken(T_WHITESPACE, ' ');
var_dump($space->isIgnorable());  // -> bool(true)
```

### 参见

-   <span class="function">PhpToken::tokenize</span>

PhpToken::\_\_toString
======================

Returns the textual content of the token.

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">PhpToken::\_\_toString</span> ( <span
class="methodparam">void</span> )

Returns the textual content of the token.

### 参数

此函数没有参数。

### 返回值

A textual content of the token.

### 范例

**示例 \#1 <span class="function">PhpToken::\_\_toString</span>
example**

``` php
<?php
$token = new PhpToken(T_ECHO, 'echo');
echo $token;
```

以上例程会输出：

    echo

### 参见

-   <span class="function">token\_name</span>

PhpToken::tokenize
==================

Splits given source into PHP tokens, represented by PhpToken objects.

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">PhpToken::tokenize</span> ( <span
class="methodparam"><span class="type">string</span> `$code`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

Returns an array of PhpToken objects representing given `code`.

### 参数

`code`  
The PHP source to parse.

`flags`  
Valid flags:

-   <span class="simpara"> **`TOKEN_PARSE`** - Recognises the ability to
    use reserved words in specific contexts. </span>

### 返回值

An array of PHP tokens represented by instances of PhpToken or its
descendants. This method returns <span class="type">static\[\]</span> so
that PhpToken can be seamlessly extended.

### 范例

**示例 \#1 <span class="function">PhpToken::tokenize</span> example**

``` php
<?php
$tokens = PhpToken::tokenize('<?php echo; ?>');

foreach ($tokens as $token) {
    echo "Line {$token->line}: {$token->getTokenName()} ('{$token->text}')", PHP_EOL;
}
```

以上例程会输出：

    Line 1: T_OPEN_TAG ('<?php ')
    Line 1: T_ECHO ('echo')
    Line 1: ; (';')
    Line 1: T_WHITESPACE (' ')
    Line 1: T_CLOSE_TAG ('?>')

**示例 \#2 Extending PhpToken**

``` php
<?php

class MyPhpToken extends PhpToken {
    public function getUpperText() {
        return strtoupper($this->text);
    }
}

$tokens = MyPhpToken::tokenize('<?php echo; ?>');
echo "'{$tokens[0]->getUpperText()}'";
```

以上例程会输出：

    '<?PHP '

### 参见

-   <span class="function">token\_get\_all</span>
