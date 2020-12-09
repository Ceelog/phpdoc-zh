Varnish
=======

**目录**

-   [简介](/intro/varnish.html)
-   [安装／配置](/varnish/setup.html)
    -   [需求](/varnish/setup.html#需求)
    -   [安装](/varnish/setup.html#安装)
    -   [运行时配置](/varnish/setup.html#运行时配置)
    -   [资源类型](/varnish/setup.html#资源类型)
-   [预定义常量](/varnish/constants.html)
-   [范例](/varnish/examples.html)
    -   [Basic VarnishAdmin
        usage](/varnish/examples.html#Basic%20VarnishAdmin%20usage)
    -   [Basic VarnishStat
        usage](/varnish/examples.html#Basic%20VarnishStat%20usage)
    -   [Basic VarnishLog
        usage](/varnish/examples.html#Basic%20VarnishLog%20usage)
-   [VarnishAdmin](/class/varnishadmin.html) — The VarnishAdmin class
    -   [VarnishAdmin::auth](/class/varnishadmin.html#VarnishAdmin::auth)
        — Authenticate on a varnish instance
    -   [VarnishAdmin::ban](/class/varnishadmin.html#VarnishAdmin::ban)
        — Ban URLs using a VCL expression
    -   [VarnishAdmin::banUrl](/class/varnishadmin.html#VarnishAdmin::banUrl)
        — Ban an URL using a VCL expression
    -   [VarnishAdmin::clearPanic](/class/varnishadmin.html#VarnishAdmin::clearPanic)
        — Clear varnish instance panic messages
    -   [VarnishAdmin::connect](/class/varnishadmin.html#VarnishAdmin::connect)
        — Connect to a varnish instance administration interface
    -   [VarnishAdmin::\_\_construct](/class/varnishadmin.html#VarnishAdmin::__construct)
        — VarnishAdmin constructor
    -   [VarnishAdmin::disconnect](/class/varnishadmin.html#VarnishAdmin::disconnect)
        — Disconnect from a varnish instance administration interface
    -   [VarnishAdmin::getPanic](/class/varnishadmin.html#VarnishAdmin::getPanic)
        — Get the last panic message on a varnish instance
    -   [VarnishAdmin::getParams](/class/varnishadmin.html#VarnishAdmin::getParams)
        — Fetch current varnish instance configuration parameters
    -   [VarnishAdmin::isRunning](/class/varnishadmin.html#VarnishAdmin::isRunning)
        — Check if the varnish slave process is currently running
    -   [VarnishAdmin::setCompat](/class/varnishadmin.html#VarnishAdmin::setCompat)
        — Set the class compat configuration param
    -   [VarnishAdmin::setHost](/class/varnishadmin.html#VarnishAdmin::setHost)
        — Set the class host configuration param
    -   [VarnishAdmin::setIdent](/class/varnishadmin.html#VarnishAdmin::setIdent)
        — Set the class ident configuration param
    -   [VarnishAdmin::setParam](/class/varnishadmin.html#VarnishAdmin::setParam)
        — Set configuration param on the current varnish instance
    -   [VarnishAdmin::setPort](/class/varnishadmin.html#VarnishAdmin::setPort)
        — Set the class port configuration param
    -   [VarnishAdmin::setSecret](/class/varnishadmin.html#VarnishAdmin::setSecret)
        — Set the class secret configuration param
    -   [VarnishAdmin::setTimeout](/class/varnishadmin.html#VarnishAdmin::setTimeout)
        — Set the class timeout configuration param
    -   [VarnishAdmin::start](/class/varnishadmin.html#VarnishAdmin::start)
        — Start varnish worker process
    -   [VarnishAdmin::stop](/class/varnishadmin.html#VarnishAdmin::stop)
        — Stop varnish worker process
-   [VarnishStat](/class/varnishstat.html) — The VarnishStat class
    -   [VarnishStat::\_\_construct](/class/varnishstat.html#VarnishStat::__construct)
        — VarnishStat constructor
    -   [VarnishStat::getSnapshot](/class/varnishstat.html#VarnishStat::getSnapshot)
        — Get the current varnish instance statistics snapshot
-   [VarnishLog](/class/varnishlog.html) — The VarnishLog class
    -   [VarnishLog::\_\_construct](/class/varnishlog.html#VarnishLog::__construct)
        — Varnishlog constructor
    -   [VarnishLog::getLine](/class/varnishlog.html#VarnishLog::getLine)
        — Get next log line
    -   [VarnishLog::getTagName](/class/varnishlog.html#VarnishLog::getTagName)
        — Get the log tag string representation by its index

简介
----

类摘要
------

**VarnishAdmin**

<span class="ooclass"> class **VarnishAdmin** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">auth</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">ban</span> ( <span class="methodparam"><span
class="type">string</span> `$vcl_regex`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">banUrl</span> ( <span class="methodparam"><span
class="type">string</span> `$vcl_regex`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">clearPanic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">connect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">disconnect</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPanic</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getParams</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isRunning</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setCompat</span> ( <span
class="methodparam"><span class="type">int</span> `$compat`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setHost</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setIdent</span> ( <span
class="methodparam"><span class="type">string</span> `$ident`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">setParam</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type"><span
class="type">string</span><span class="type">int</span></span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setPort</span> ( <span
class="methodparam"><span class="type">int</span> `$port`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSecret</span> ( <span
class="methodparam"><span class="type">string</span> `$secret`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">start</span> ( <span class="methodparam">void</span>
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">stop</span> ( <span class="methodparam">void</span> )

}

VarnishAdmin::auth
==================

Authenticate on a varnish instance

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">VarnishAdmin::auth</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

VarnishAdmin::ban
=================

Ban URLs using a VCL expression

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::ban</span> ( <span
class="methodparam"><span class="type">string</span> `$vcl_regex`</span>
)

### 参数

`vcl_regex`  
Varnish VCL expression. It's based on the varnish ban command.

### 返回值

Returns the varnish command status.

VarnishAdmin::banUrl
====================

Ban an URL using a VCL expression

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::banUrl</span> ( <span
class="methodparam"><span class="type">string</span> `$vcl_regex`</span>
)

### 参数

`vcl_regex`  
URL regular expression in PCRE compatible syntax. It's based on the
ban.url varnish command.

### 返回值

Returns the varnish command status.

VarnishAdmin::clearPanic
========================

Clear varnish instance panic messages

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::clearPanic</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the varnish command status.

VarnishAdmin::connect
=====================

Connect to a varnish instance administration interface

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">VarnishAdmin::connect</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

VarnishAdmin::\_\_construct
===========================

VarnishAdmin constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">VarnishAdmin::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

### 参数

`args`  
Configuration arguments. The possible keys are:

``` parameters
VARNISH_CONFIG_IDENT - local varnish instance ident
VARNISH_CONFIG_HOST - varnish instance ip
VARNISH_CONFIG_PORT - varnish instance port
VARNISH_CONFIG_SECRET - varnish instance secret
VARNISH_CONFIG_TIMEOUT - connection read timeout
VARNISH_CONFIG_COMPAT - varnish major version compatibility
```

### 返回值

### 范例

**示例 \#1 <span class="function">VarnishAdmin::\_\_construct</span>
example**

``` php
<?php
    $args = array(
        VARNISH_CONFIG_HOST => "::1",
        VARNISH_CONFIG_PORT => 6082,
        VARNISH_CONFIG_SECRET => "5174826b-8595-4958-aa7a-0609632ad7ca",
        VARNISH_CONFIG_TIMEOUT => 300,
    );
    $va = new VarnishAdmin($args);
?>
```

VarnishAdmin::disconnect
========================

Disconnect from a varnish instance administration interface

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">VarnishAdmin::disconnect</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

VarnishAdmin::getPanic
======================

Get the last panic message on a varnish instance

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">VarnishAdmin::getPanic</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the last panic message on the current varnish instance.

VarnishAdmin::getParams
=======================

Fetch current varnish instance configuration parameters

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">VarnishAdmin::getParams</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an array with the varnish configuration parameters.

VarnishAdmin::isRunning
=======================

Check if the varnish slave process is currently running

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">VarnishAdmin::isRunning</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

VarnishAdmin::setCompat
=======================

Set the class compat configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setCompat</span> ( <span
class="methodparam"><span class="type">int</span> `$compat`</span> )

### 参数

`compat`  
Varnish compatibility option.

### 返回值

VarnishAdmin::setHost
=====================

Set the class host configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setHost</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> )

### 参数

`host`  
Connection host configuration parameter.

### 返回值

VarnishAdmin::setIdent
======================

Set the class ident configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setIdent</span> ( <span
class="methodparam"><span class="type">string</span> `$ident`</span> )

### 参数

`ident`  
Connection ident configuration parameter.

### 返回值

VarnishAdmin::setParam
======================

Set configuration param on the current varnish instance

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::setParam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">int</span></span>
`$value`</span> )

### 参数

`name`  
Varnish configuration param name.

`value`  
Varnish configuration param value.

### 返回值

Returns the varnish command status.

VarnishAdmin::setPort
=====================

Set the class port configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setPort</span> ( <span
class="methodparam"><span class="type">int</span> `$port`</span> )

### 参数

`port`  
Connection port configuration parameter.

### 返回值

VarnishAdmin::setSecret
=======================

Set the class secret configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setSecret</span> ( <span
class="methodparam"><span class="type">string</span> `$secret`</span> )

### 参数

`secret`  
Connection secret configuration parameter.

### 返回值

VarnishAdmin::setTimeout
========================

Set the class timeout configuration param

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">VarnishAdmin::setTimeout</span> ( <span
class="methodparam"><span class="type">int</span> `$timeout`</span> )

### 参数

`timeout`  
Connection timeout configuration parameter.

### 返回值

VarnishAdmin::start
===================

Start varnish worker process

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::start</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the varnish command status.

VarnishAdmin::stop
==================

Stop varnish worker process

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">VarnishAdmin::stop</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns the varnish command status.

简介
----

类摘要
------

**VarnishStat**

<span class="ooclass"> class **VarnishStat** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getSnapshot</span> ( <span
class="methodparam">void</span> )

}

VarnishStat::\_\_construct
==========================

VarnishStat constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">VarnishStat::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

### 参数

`args`  
Configuration arguments. The possible keys are:

``` parameters
VARNISH_CONFIG_IDENT - local varnish instance ident path
```

### 返回值

VarnishStat::getSnapshot
========================

Get the current varnish instance statistics snapshot

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">VarnishStat::getSnapshot</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Array with the varnish statistic snapshot. The array keys are identical
to that in the varnishstat tool.

简介
----

类摘要
------

**VarnishLog**

<span class="ooclass"> class **VarnishLog** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Debug` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Error` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_CLI` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_StatSess` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ReqEnd` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_SessionOpen` <span class="initializer"> = 5</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_SessionClose` <span class="initializer"> = 6</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_BackendOpen` <span class="initializer"> = 7</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_BackendXID` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_BackendReuse` <span class="initializer"> = 9</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_BackendClose` <span class="initializer"> = 10</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_HttpGarbage` <span class="initializer"> = 11</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Backend` <span class="initializer"> = 12</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Length` <span class="initializer"> = 13</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_FetchError` <span class="initializer"> = 14</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxRequest` <span class="initializer"> = 15</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxResponse` <span class="initializer"> = 16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxStatus` <span class="initializer"> = 17</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxURL` <span class="initializer"> = 18</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxProtocol` <span class="initializer"> = 19</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_RxHeader` <span class="initializer"> = 20</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxRequest` <span class="initializer"> = 21</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxResponse` <span class="initializer"> = 22</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxStatus` <span class="initializer"> = 23</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxURL` <span class="initializer"> = 24</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxProtocol` <span class="initializer"> = 25</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TxHeader` <span class="initializer"> = 26</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjRequest` <span class="initializer"> = 27</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjResponse` <span class="initializer"> = 28</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjStatus` <span class="initializer"> = 29</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjURL` <span class="initializer"> = 30</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjProtocol` <span class="initializer"> = 31</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ObjHeader` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_LostHeader` <span class="initializer"> = 33</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_TTL` <span class="initializer"> = 34</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Fetch_Body` <span class="initializer"> = 35</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_acl` <span class="initializer"> = 36</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_call` <span class="initializer"> = 37</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_trace` <span class="initializer"> = 38</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_return` <span class="initializer"> = 39</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_error` <span class="initializer"> = 40</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ReqStart` <span class="initializer"> = 41</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Hit` <span class="initializer"> = 42</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_HitPass` <span class="initializer"> = 43</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ExpBan` <span class="initializer"> = 44</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ExpKill` <span class="initializer"> = 45</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_WorkThread` <span class="initializer"> = 46</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_ESI_xmlerror` <span class="initializer"> = 47</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Hash` <span class="initializer"> = 48</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Backend_health` <span class="initializer"> = 49</span>
;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_VCL_Log` <span class="initializer"> = 50</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`VarnishLog::TAG_Gzip` <span class="initializer"> = 51</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">getTagName</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

}

预定义常量
----------

**`VarnishLog::TAG_Debug`**  

**`VarnishLog::TAG_Error`**  

**`VarnishLog::TAG_CLI`**  

**`VarnishLog::TAG_StatSess`**  

**`VarnishLog::TAG_ReqEnd`**  

**`VarnishLog::TAG_SessionOpen`**  

**`VarnishLog::TAG_SessionClose`**  

**`VarnishLog::TAG_BackendOpen`**  

**`VarnishLog::TAG_BackendXID`**  

**`VarnishLog::TAG_BackendReuse`**  

**`VarnishLog::TAG_BackendClose`**  

**`VarnishLog::TAG_HttpGarbage`**  

**`VarnishLog::TAG_Backend`**  

**`VarnishLog::TAG_Length`**  

**`VarnishLog::TAG_FetchError`**  

**`VarnishLog::TAG_RxRequest`**  

**`VarnishLog::TAG_RxResponse`**  

**`VarnishLog::TAG_RxStatus`**  

**`VarnishLog::TAG_RxURL`**  

**`VarnishLog::TAG_RxProtocol`**  

**`VarnishLog::TAG_RxHeader`**  

**`VarnishLog::TAG_TxRequest`**  

**`VarnishLog::TAG_TxResponse`**  

**`VarnishLog::TAG_TxStatus`**  

**`VarnishLog::TAG_TxURL`**  

**`VarnishLog::TAG_TxProtocol`**  

**`VarnishLog::TAG_TxHeader`**  

**`VarnishLog::TAG_ObjRequest`**  

**`VarnishLog::TAG_ObjResponse`**  

**`VarnishLog::TAG_ObjStatus`**  

**`VarnishLog::TAG_ObjURL`**  

**`VarnishLog::TAG_ObjProtocol`**  

**`VarnishLog::TAG_ObjHeader`**  

**`VarnishLog::TAG_LostHeader`**  

**`VarnishLog::TAG_TTL`**  

**`VarnishLog::TAG_Fetch_Body`**  

**`VarnishLog::TAG_VCL_acl`**  

**`VarnishLog::TAG_VCL_call`**  

**`VarnishLog::TAG_VCL_trace`**  

**`VarnishLog::TAG_VCL_return`**  

**`VarnishLog::TAG_VCL_error`**  

**`VarnishLog::TAG_ReqStart`**  

**`VarnishLog::TAG_Hit`**  

**`VarnishLog::TAG_HitPass`**  

**`VarnishLog::TAG_ExpBan`**  

**`VarnishLog::TAG_ExpKill`**  

**`VarnishLog::TAG_WorkThread`**  

**`VarnishLog::TAG_ESI_xmlerror`**  

**`VarnishLog::TAG_Hash`**  

**`VarnishLog::TAG_Backend_health`**  

**`VarnishLog::TAG_VCL_Log`**  

**`VarnishLog::TAG_Gzip`**  

VarnishLog::\_\_construct
=========================

Varnishlog constructor

### 说明

<span class="modifier">public</span> <span
class="methodname">VarnishLog::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">array</span> `$args`</span> \] )

### 参数

`args`  
Configuration arguments. The possible keys are:

``` parameters
VARNISH_CONFIG_IDENT - local varnish instance ident path
```

### 返回值

VarnishLog::getLine
===================

Get next log line

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">VarnishLog::getLine</span> ( <span
class="methodparam">void</span> )

### 参数

此函数没有参数。

### 返回值

Returns an array with the log line data.

VarnishLog::getTagName
======================

Get the log tag string representation by its index

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">string</span> <span
class="methodname">VarnishLog::getTagName</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

### 参数

`index`  
Log tag index.

### 返回值

Returns the log tag name as <span class="type">string</span>.
