Yet Another RPC Framework
=========================

**目录**

-   [简介](/intro/yar.html)
-   [安装／配置](/yar/setup.html)
    -   [需求](/yar/setup.html#需求)
    -   [安装](/yar/setup.html#安装)
    -   [运行时配置](/yar/setup.html#运行时配置)
    -   [资源类型](/yar/setup.html#资源类型)
-   [预定义常量](/yar/constants.html)
-   [范例](/yar/examples.html)
-   [Yar\_Server](/class/yar-server.html) — The Yar\_Server class
    -   [Yar\_Server::\_\_construct](/class/yar-server.html#Yar_Server::__construct)
        — 创建一个HTTP RPC Server
    -   [Yar\_Server::handle](/class/yar-server.html#Yar_Server::handle)
        — 启动HTTP RPC Server
-   [Yar\_Client](/class/yar-client.html) — The Yar\_Client class
    -   [Yar\_Client::\_\_call](/class/yar-client.html#Yar_Client::__call)
        — 调用远程服务
    -   [Yar\_Client::\_\_construct](/class/yar-client.html#Yar_Client::__construct)
        — 创建一个客户端实例
    -   [Yar\_Client::setOpt](/class/yar-client.html#Yar_Client::setOpt)
        — 设置调用的配置
-   [Yar\_Concurrent\_Client](/class/yar-concurrent-client.html) — The
    Yar\_Concurrent\_Client class
    -   [Yar\_Concurrent\_Client::call](/class/yar-concurrent-client.html#Yar_Concurrent_Client::call)
        — 注册一个并行的服务调用
    -   [Yar\_Concurrent\_Client::loop](/class/yar-concurrent-client.html#Yar_Concurrent_Client::loop)
        — 发送所有注册的并行调用
    -   [Yar\_Concurrent\_Client::reset](/class/yar-concurrent-client.html#Yar_Concurrent_Client::reset)
        — Clean all registered calls
-   [Yar\_Server\_Exception](/class/yar-server-exception.html) — The
    Yar\_Server\_Exception class
    -   [Yar\_Server\_Exception::getType](/class/yar-server-exception.html#Yar_Server_Exception::getType)
        — 获取异常的原始类型
-   [Yar\_Client\_Exception](/class/yar-client-exception.html) — The
    Yar\_Client\_Exception class
    -   [Yar\_Client\_Exception::getType](/class/yar-client-exception.html#Yar_Client_Exception::getType)
        — The getType purpose

简介
----

类摘要
------

**Yar\_Server**

<span class="ooclass"> class **Yar\_Server** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_executor` ;

/\* 方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">Object</span> `$obj`</span> )

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">handle</span> ( <span
class="methodparam">void</span> )

}

属性
----

`_executor`  

Yar\_Server::\_\_construct
==========================

创建一个HTTP RPC Server

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">Yar\_Server::\_\_construct</span> ( <span
class="methodparam"><span class="type">Object</span> `$obj`</span> )

创建一个Yar的HTTP RPC服务，参数 $obj
对象的所有公开方法都会被注册为服务函数， 可以被RPC调用。

### 参数

`obj`  
一个对象实例, 这个对象的所有公开方法都会被注册为服务函数.

### 返回值

返回一个<span class="classname">Yar\_Server</span>的实例。

### 范例

**示例 \#1 <span
class="function">Yar\_Server::\_\_construct</span>示例**

``` php
<?php
class API {
    /**
     * the doc info will be generated automatically into service info page.
     * @params 
     * @return
     */
    public function some_method($parameter, $option = "foo") {
         return "some_method";
    }

    protected function client_can_not_see() {
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Server::handle</span>

Yar\_Server::handle
===================

启动HTTP RPC Server

### 说明

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">Yar\_Server::handle</span> ( <span
class="methodparam">void</span> )

启动服务, 开始接受客户端的调用请求.

> **Note**:
>
> 来自客户端的调用, 都是通过POST请求发送过来的.
> 如果一个GET请求访问到这个Server, 那在yar.expose\_info开启的情况下,
> 这个服务的Server Info信息会被展现.

### 参数

此函数没有参数。

### 返回值

boolean

### 范例

**示例 \#1 <span class="function">Yar\_Server::handle</span>示例**

``` php
<?php
class API {
    /**
     * the doc info will be generated automatically into service info page.
     * @params 
     * @return
     */
    public function some_method($parameter, $option = "foo") {
    }

    protected function client_can_not_see() {
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Server::\_\_construct</span>

简介
----

类摘要
------

**Yar\_Client**

<span class="ooclass"> class **Yar\_Client** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_protocol` ;

<span class="modifier">protected</span> `$_uri` ;

<span class="modifier">protected</span> `$_options` ;

<span class="modifier">protected</span> `$_running` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_call</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> ,
<span class="methodparam"><span class="type">array</span>
`$parameters`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$url`</span> )

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">setOpt</span> ( <span class="methodparam"><span
class="type">number</span> `$name`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

}

属性
----

`_protocol`  

`_uri`  

`_options`  

`_running`  

Yar\_Client::\_\_call
=====================

调用远程服务

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yar\_Client::\_\_call</span> ( <span
class="methodparam"><span class="type">string</span> `$method`</span> ,
<span class="methodparam"><span class="type">array</span>
`$parameters`</span> )

发起一个RPC调用, 并且得到返回值. 如果服务端的远程调用抛出异常,
那么本地也会相应的抛出一个<span
class="classname">Yar\_Server\_Exception</span>异常.

### 参数

`method`  
远程服务的名字.

`parameters`  
调用参数.

### 返回值

### 范例

**示例 \#1 <span class="function">Yar\_Client::\_\_call</span> example**

``` php
<?php

$client = new Yar_Client("http://host/api/");

/* 调用远程服务的some_method服务 */
$result = $client->some_method("parameter");

?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Client::setOpt</span>

Yar\_Client::\_\_construct
==========================

创建一个客户端实例

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="methodname">Yar\_Client::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$url`</span> )

创建一个<span class="classname">Yar\_Client</span> 到一个 <span
class="classname">Yar\_Server</span>的实例.

### 参数

`url`  
服务端的HTTP URL路径.

### 返回值

<span class="classname">Yar\_Client</span>实例.

### 范例

**示例 \#1 <span
class="function">Yar\_Client::\_\_construct</span>示例**

``` php
<?php
$client = new Yar_Client("http://host/api/");
?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Client::\_\_call</span>
-   <span class="methodname">Yar\_Client::setOpt</span>

Yar\_Client::setOpt
===================

设置调用的配置

### 说明

<span class="modifier">public</span> <span class="type">boolean</span>
<span class="methodname">Yar\_Client::setOpt</span> ( <span
class="methodparam"><span class="type">number</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

设置调用远程服务的一些配置, 比如超时值, 打包类型等.

### 参数

`name`  
可以是: YAR\_OPT\_PACKAGER, YAR\_OPT\_PERSISTENT
(需要服务端支持keepalive), YAR\_OPT\_TIMEOUT, YAR\_OPT\_CONNECT\_TIMEOUT

`value`  

### 返回值

### 范例

**示例 \#1 <span class="function">Yar\_Client::setOpt</span>示例**

``` php
<?php

$cient = new Yar_Client("http://host/api/");

//Set timeout to 1s
$client->SetOpt(YAR_OPT_CONNECT_TIMEOUT, 1000);

//Set packager to JSON
$client->SetOpt(YAR_OPT_PACKAGER, "json");

/* call remote service */
$result = $client->some_method("parameter");
?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Client::\_\_call</span>

简介
----

类摘要
------

**Yar\_Concurrent\_Client**

<span class="ooclass"> class **Yar\_Concurrent\_Client** </span> {

/\* 属性 \*/

<span class="modifier">static</span> `$_callstack` ;

<span class="modifier">static</span> `$_callback` ;

<span class="modifier">static</span> `$_error_callback` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">call</span> ( <span class="methodparam"><span
class="type">string</span> `$uri`</span> , <span
class="methodparam"><span class="type">string</span> `$method`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$parameters`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$error_callback`</span> \[, <span class="methodparam"><span
class="type">array</span> `$options`</span> \]\]\]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">boolean</span> <span
class="methodname">loop</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$error_callback`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">reset</span> ( <span class="methodparam">void</span>
)

}

属性
----

`_callstack`  

`_callback`  

`_error_callback`  

Yar\_Concurrent\_Client::call
=============================

注册一个并行的服务调用

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">int</span> <span
class="methodname">Yar\_Concurrent\_Client::call</span> ( <span
class="methodparam"><span class="type">string</span> `$uri`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method`</span> \[, <span class="methodparam"><span
class="type">array</span> `$parameters`</span> \[, <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$error_callback`</span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\]\]\] )

注册一个并行的(异步的)远程服务调用, 不过这个调用请求不会被立即发出,
而是会在接下来调用 <span
class="methodname">Yar\_Concurrent\_Client::loop</span>的时候才真正的发送出去.

### 参数

`uri`  
RPC 服务的 URI(http 或 tcp).

`method`  
调用的服务名字(也就是服务方法名).

`parameters`  
调用的参数.

`callback`  
回调函数, 在远程服务的返回到达的时候被Yar调用, 从而可以处理返回内容.

### 返回值

唯一 ID， 可用于区分到底是那个调用的返回.

### 范例

**示例 \#1 <span
class="function">Yar\_Concurrent\_Client::call</span>示例**

``` php
<?php
function callback($retval, $callinfo) {
     var_dump($retval);
}

function error_callback($type, $error, $callinfo) {
    error_log($error);
}

Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback");
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"));   // if the callback is not specificed, 
                                                                               // callback in loop will be used
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_PACKAGER => "json"));
                                                                               //this server accept json packager
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_TIMEOUT=>1));
                                                                               //custom timeout 

// 这个时候请求都还没有发出
?>
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Concurrent\_Client::loop</span>
-   <span class="methodname">Yar\_Concurrent\_Client::reset</span>
-   <span class="methodname">Yar\_Server::\_\_construct</span>
-   <span class="methodname">Yar\_Server::handle</span>

Yar\_Concurrent\_Client::loop
=============================

发送所有注册的并行调用

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">boolean</span> <span
class="methodname">Yar\_Concurrent\_Client::loop</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$error_callback`</span> \]\] )

发送所有的已经通过 <span
class="methodname">Yar\_Concurrent\_Client::call</span>注册的并行调用,
并且等待返回.

### 参数

`callback`  
如果这个回掉函数被设置,
那么Yar在发送出所有的请求之后立即调用一次这个回掉函数(此时还没有任何请求返回),
调用的时候$callinfo参数是NULL.

如果在注册并行调用的时候制定了callback, 那么那个callback有更高的优先级.

`error_callback`  
错误回掉函数, 如果设置了, 那么Yar在出错的时候会调用这个回掉函数.

### 返回值

### 范例

**示例 \#1 <span class="function">Yar\_Concurrent\_Client::loop</span>
example**

``` php
<?php
function callback($retval, $callinfo) {
     if ($callinfo == NULL) {
        echo "现在, 所有的请求都发出去了, 还没有任何请求返回\n";
     } else {
              echo "这是一个远程调用的返回, 调用的服务名是", $callinfo["method"], 
                      ". 调用的sequence是 " , $callinfo["sequence"] , "\n";
        var_dump($retval);
     }
} 

function error_callback($type, $error, $callinfo) {
    error_log($error);
}

Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback");
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"));   // if the callback is not specificed, 
                                                                               // callback in loop will be used
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_PACKAGER => "json"));
                                                                               //this server accept json packager
Yar_Concurrent_Client::call("http://host/api/", "some_method", array("parameters"), "callback", NULL, array(YAR_OPT_TIMEOUT=>1));
                                                                               //custom timeout 

Yar_Concurrent_Client::loop("callback", "error_callback"); //send the requests, 
                                                           //the error_callback is optional
?>
```

以上例程的输出类似于：

    现在, 所有的请求都发出去了, 还没有任何请求返回
    这是一个远程调用的返回, 调用的服务名是some_method, 调用的sequence是 4
    string(11) "some_method"
    这是一个远程调用的返回, 调用的服务名是some_method, 调用的sequence是 1
    string(11) "some_method"
    这是一个远程调用的返回, 调用的服务名是some_method, 调用的sequence是 2
    string(11) "some_method"
    这是一个远程调用的返回, 调用的服务名是some_method, 调用的sequence是 3
    string(11) "some_method"

### 参见

-   <span class="methodname">Yar\_Concurrent\_Client::call</span>
-   <span class="methodname">Yar\_Server::\_\_construct</span>
-   <span class="methodname">Yar\_Server::handle</span>

Yar\_Concurrent\_Client::reset
==============================

Clean all registered calls

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">bool</span> <span
class="methodname">Yar\_Concurrent\_Client::reset</span> ( <span
class="methodparam">void</span> )

Clean all registered calls

### 参数

### 返回值

### 范例

**示例 \#1 <span class="function">Yar\_Concurrent\_Client::reset</span>
example**

``` php
```

以上例程的输出类似于：

### 参见

-   <span class="methodname">Yar\_Concurrent\_Client::call</span>
-   <span class="methodname">Yar\_Concurrent\_Client::loop</span>
-   <span class="methodname">Yar\_Server::\_\_construct</span>
-   <span class="methodname">Yar\_Server::handle</span>

简介
----

If service threw exceptions, A Yar\_Server\_Exception will be threw in
client side.

类摘要
------

**Yar\_Server\_Exception**

<span class="ooclass"> class **Yar\_Server\_Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> `$_type` ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getType</span> ( <span
class="methodparam">void</span> )

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
<span class="type">mixed</span> <span
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

属性
----

`message`  

`code`  

`file`  

`line`  

`_type`  

Yar\_Server\_Exception::getType
===============================

获取异常的原始类型

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Yar\_Server\_Exception::getType</span> ( <span
class="methodparam">void</span> )

当服务端的服务函数抛出异常的时候, 客户端本地会响应的抛出一个<span
class="classname">Yar\_Server\_Exception</span>异常. 有一个属性,
标明了服务端异常的类型. 这个方法就是获取这个异常类型.

### 参数

此函数没有参数。

### 返回值

string

### 范例

**示例 \#1 <span
class="function">Yar\_Server\_Exception::getType</span>示例**

``` php
//Server.php
<?php
class Custom_Exception extends Exception {};

class API {
    public function throw_exception($name) {
        throw new Custom_Exception($name);
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>

//Client.php
<?php
$client = new Yar_Client("http://host/api.php");

try {
    $client->throw_exception("client");
} catch (Yar_Server_Exception $e) {
    var_dump($e->getType());
    var_dump($e->getMessage());
}
```

以上例程的输出类似于：

    string(16) "Custom_Exception"
    string(6) "client"

### 参见

-   

简介
----

类摘要
------

**Yar\_Client\_Exception**

<span class="ooclass"> class **Yar\_Client\_Exception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">getType</span> ( <span
class="methodparam">void</span> )

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
<span class="type">mixed</span> <span
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

属性
----

`message`  

`code`  

`file`  

`line`  

Yar\_Client\_Exception::getType
===============================

The getType purpose

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Yar\_Client\_Exception::getType</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

### 范例

**示例 \#1 <span class="function">Yar\_Client\_Exception::getType</span>
example**

``` php
<?php

/* ... */

?>
```

以上例程的输出类似于：

    ...

### 参见

-   
