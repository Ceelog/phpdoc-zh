libxml
======

**目录**

-   [简介](/intro/libxml.html)
-   [安装／配置](/libxml/setup.html)
    -   [需求](/libxml/setup.html#需求)
    -   [安装](/libxml/setup.html#安装)
    -   [运行时配置](/libxml/setup.html#运行时配置)
    -   [资源类型](/libxml/setup.html#资源类型)
-   [预定义常量](/libxml/constants.html)
-   [libXMLError](/class/libxmlerror.html) — The libXMLError class
-   [libxml 函数](/ref/libxml.html)
    -   [libxml\_clear\_errors](/ref/libxml.html#libxml_clear_errors) —
        Clear libxml error buffer
    -   [libxml\_disable\_entity\_loader](/ref/libxml.html#libxml_disable_entity_loader)
        — Disable the ability to load external entities
    -   [libxml\_get\_errors](/ref/libxml.html#libxml_get_errors) —
        Retrieve array of errors
    -   [libxml\_get\_last\_error](/ref/libxml.html#libxml_get_last_error)
        — Retrieve last error from libxml
    -   [libxml\_set\_external\_entity\_loader](/ref/libxml.html#libxml_set_external_entity_loader)
        — Changes the default external entity loader
    -   [libxml\_set\_streams\_context](/ref/libxml.html#libxml_set_streams_context)
        — Set the streams context for the next libxml document load or
        write
    -   [libxml\_use\_internal\_errors](/ref/libxml.html#libxml_use_internal_errors)
        — Disable libxml errors and allow user to fetch error
        information as needed

简介
----

Contains various information about errors thrown by libxml. The error
codes are described within the official
<a href="http://www.xmlsoft.org/html/libxml-xmlerror.html" class="link external">» xmlError API documentation</a>.

类摘要
------

**libXMLError**

<span class="ooclass"> class **libXMLError** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">int</span>
`$level` ;

<span class="modifier">public</span> <span class="type">int</span>
`$code` ;

<span class="modifier">public</span> <span class="type">int</span>
`$column` ;

<span class="modifier">public</span> <span class="type">string</span>
`$message` ;

<span class="modifier">public</span> <span class="type">string</span>
`$file` ;

<span class="modifier">public</span> <span class="type">int</span>
`$line` ;

}

属性
----

`level`  
the severity of the error (one of the following constants:
**`LIBXML_ERR_WARNING`**, **`LIBXML_ERR_ERROR`** or
**`LIBXML_ERR_FATAL`**)

`code`  
The error's code.

`column`  
The column where the error occurred.

> **Note**:
>
> This property isn't entirely implemented in libxml and therefore *0*
> is often returned.

`message`  
The error message, if any.

`file`  
The filename, or empty if the XML was loaded from a string.

`line`  
The line where the error occurred.
