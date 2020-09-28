checkdnsrr
==========

给指定的主机（域名）或者IP地址做DNS通信检查

### 说明

<span class="type">bool</span> <span
class="methodname">checkdnsrr</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> \[, <span
class="methodparam"><span class="type">string</span> `$type`<span
class="initializer"> = "MX"</span></span> \] )

根据不同记录（`type`）类型查询主机（`host`）相应的DNS记录。

### 参数

`host`  
主机（`host`）可以是一个IP地址也可以是域名。

`type`  
解析记录类型（`type`）可能是下面这些类型中的任何一个：A，MX，NS，SOA，PTR，CNAME，AAAA，A6，
SRV，NAPTR，TXT 或者 ANY。

### 返回值

如果记录能找到，就返回**`TRUE`**；如果查找不到该DNS记录或者发生了错误，就返回**`FALSE`**。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 5.3.0 | 这个函数在Windows平台上也可以使用了。 |
| 5.2.4 | 增加了TXT的记录`类型`。               |
| 5.0.0 | 增加了AAAA的记录`类型`。              |

### 注释

> **Note**:
>
> 出于对低版本在windows平台上的兼容性，可以试试<a href="https://pear.php.net/" class="link external">» PEAR</a>扩展包里面提供的
> <a href="https://pear.php.net/package/Net_DNS" class="link external">» Net_DNS</a>类。

### 参见

-   <span class="function">dns\_get\_record</span>
-   <span class="function">getmxrr</span>
-   <span class="function">gethostbyaddr</span>
-   <span class="function">gethostbyname</span>
-   <span class="function">gethostbynamel</span>
-   the named(8) manual page

closelog
========

关闭系统日志链接

### 说明

<span class="type">bool</span> <span class="methodname">closelog</span>
( <span class="methodparam">void</span> )

<span class="function">closelog</span>
关闭用于通信的描述符并写入系统日志。<span
class="function">closelog</span>是可选的。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">syslog</span>
-   <span class="function">openlog</span>

define\_syslog\_variables
=========================

Initializes all syslog related variables

### 说明

<span class="type">void</span> <span
class="methodname">define\_syslog\_variables</span> ( <span
class="methodparam">void</span> )

Initializes all variables used in the syslog functions.

### 返回值

没有返回值。

| Variable        | Constant equal     | Meaning                   | Notes                                |
|-----------------|--------------------|---------------------------|--------------------------------------|
| `$LOG_EMERG`    | **`LOG_EMERG`**    | System is unusable        |                                      |
| `$LOG_ALERT`    | **`LOG_ALERT`**    | Immediate action required |                                      |
| `$LOG_CRIT`     | **`LOG_CRIT`**     | Critical conditions       |                                      |
| `$LOG_ERR`      | **`LOG_ERR`**      |                           |                                      |
| `$LOG_WARNING`  | **`LOG_WARNING`**  |                           |                                      |
| `$LOG_NOTICE`   | **`LOG_NOTICE`**   |                           |                                      |
| `$LOG_INFO`     | **`LOG_INFO`**     |                           |                                      |
| `$LOG_DEBUG`    | **`LOG_DEBUG`**    |                           |                                      |
| `$LOG_KERN`     | **`LOG_KERN`**     |                           |                                      |
| `$LOG_USER`     | **`LOG_USER`**     | Genetic user level        |                                      |
| `$LOG_MAIL`     | **`LOG_MAIL`**     | Log to email              |                                      |
| `$LOG_DAEMON`   | **`LOG_DAEMON`**   | Other system daemons      |                                      |
| `$LOG_AUTH`     | **`LOG_AUTH`**     |                           |                                      |
| `$LOG_SYSLOG`   | **`LOG_SYSLOG`**   |                           | Not available on Netware             |
| `$LOG_LPR`      | **`LOG_LPR`**      |                           |                                      |
| `$LOG_NEWS`     | **`LOG_NEWS`**     | Usenet new                | Not available on HP-UX               |
| `$LOG_CRON`     | **`LOG_CRON`**     |                           | Not available on all platforms       |
| `$LOG_AUTHPRIV` | **`LOG_AUTHPRIV`** |                           | Not available on AIX                 |
| `$LOG_LOCAL0`   | **`LOG_LOCAL0`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL1`   | **`LOG_LOCAL1`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL2`   | **`LOG_LOCAL2`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL3`   | **`LOG_LOCAL3`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL4`   | **`LOG_LOCAL4`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL5`   | **`LOG_LOCAL5`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL6`   | **`LOG_LOCAL6`**   |                           | Not available on Windows and Netware |
| `$LOG_LOCAL7`   | **`LOG_LOCAL7`**   |                           | Not available on Windows and Netware |
| `$LOG_PID`      | **`LOG_PID`**      |                           |                                      |
| `$LOG_CONS`     | **`LOG_CONS`**     |                           |                                      |
| `$LOG_ODELAY`   | **`LOG_ODELAY`**   |                           |                                      |
| `$LOG_NDELAY`   | **`LOG_NDELAY`**   |                           |                                      |
| `$LOG_NOWAIT`   | **`LOG_NOWAIT`**   |                           | Not available on BeOS                |
| `$LOG_PERROR`   | **`LOG_PERROR`**   |                           | Not available on AIX                 |

**Warning**

本函数已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

### 范例

**示例 \#1 <span class="function">define\_syslog\_variables</span>
example**

``` php
<?php
// Check if syslog variables already is defined
if(!get_cfg_var('define_syslog_variables'))
{
    define_syslog_variables();
}

// Open the log
openlog('', $LOG_ODELAY, $LOG_MAIL | $LOG_USER);

// Continue script ...
?>
```

### 更新日志

| 版本  | 说明                                              |
|-------|---------------------------------------------------|
| 5.4.0 | This function was removed from PHP.               |
| 5.3.0 | This function now throws an E\_DEPRECATED notice. |

### 参见

-   <span class="function">openlog</span>
-   <span class="function">syslog</span>
-   <span class="function">closelog</span>

dns\_check\_record
==================

别名 <span class="function">checkdnsrr</span>

### 说明

此函数是该函数的别名： <span class="function">checkdnsrr</span>。

dns\_get\_mx
============

别名 <span class="function">getmxrr</span>

### 说明

此函数是该函数的别名： <span class="function">getmxrr</span>。

dns\_get\_record
================

获取指定主机的DNS记录

### 说明

<span class="type">array</span> <span
class="methodname">dns\_get\_record</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
\[, <span class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = DNS\_ANY</span></span> \[, <span
class="methodparam"><span class="type">array</span> `&$authns`</span>
\[, <span class="methodparam"><span class="type">array</span>
`&$addtl`</span> \[, <span class="methodparam"><span
class="type">bool</span> `&$raw`<span class="initializer"> =
false</span></span> \]\]\]\] )

获取指定主机（`hostname`）的DNS记录。

### 参数

`hostname`  
主机名（`hostname`）应该是一个DNS解析生效的域名，例如“*www.example.com*”。主机名也可以是通过对逆向解析域做DNS逆向域名解析而得到，但是在大多数情况下<span
class="function">gethostbyaddr</span>更加适合做逆向域名解析。

> **Note**:
>
> 每个DNS标准，邮件地址必须是*user.host*这样的格式（例如*hostmaster.example.com*而不是*hostmaster@example.com*），在使用<span
> class="function">mail</span>这个函数之前请检查这个值，有必要的话还需要修改。

`type`  
默认情况下，<span
class="function">dns\_get\_record</span>将会搜索所有与`hostname`相关的记录，可以通过设置`type`来限定查询。`type`的值可以是下面的其中的任何一个：
**`DNS_A`**，**`DNS_CNAME`**，**`DNS_HINFO`**，**`DNS_MX`**，**`DNS_NS`**，**`DNS_PTR`**，**`DNS_SOA`**，**`DNS_TXT`**，**`DNS_AAAA`**，**`DNS_SRV`**，**`DNS_NAPTR`**，**`DNS_A6`**，**`DNS_ALL`**或者**`DNS_ANY`**。

> **Note**:
>
> 由于dns在各个平台上表现有些不一样，**`DNS_ANY`**不会总是返回所有的记录，**`DNS_ALL`**虽然慢一些，但是会得到所有的记录，所以使用DNS\_ALL更加可靠些。

`authns`  
以引用方式传递，如果写了该参数，那么将会得到该解析记录的DNS服务器（*Authoritative
Name Servers*）的信息。

`addtl`  
以引用方式传递，如果填写了该参数，将会得到*其他所有的DNS解析记录*。

`raw`  
在原生模式下，在进行额外的查询的时候之前我们只执行请求的DNS类型，而不是循环查询所有的类型。

### 返回值

这个函数返回一个关联数组，如果失败则 或者在失败时返回
**`FALSE`**。每个关联数组都至少包含了以下的这些键。 *at minimum* the
following keys:

| Attribute | Meaning                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| host      | The record in the DNS namespace to which the rest of the associated data refers.                                                                                                                                              |
| class     | <span class="function">dns\_get\_record</span> only returns Internet class records and as such this parameter will always return *IN*.                                                                                        |
| type      | String containing the record type. Additional attributes will also be contained in the resulting array dependant on the value of type. See table below.                                                                       |
| ttl       | *"Time To Live"* remaining for this record. This will *not* equal the record's original ttl, but will rather equal the original ttl minus whatever length of time has passed since the authoritative name server was queried. |

| Type                | Extra Columns                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *A*                 | *ip*: An IPv4 addresses in dotted decimal notation.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *MX*                | *pri*: Priority of mail exchanger. Lower numbers indicate greater priority. *target*: FQDN of the mail exchanger. See also <span class="function">dns\_get\_mx</span>.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *CNAME*             | *target*: FQDN of location in DNS namespace to which the record is aliased.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *NS*                | *target*: FQDN of the name server which is authoritative for this hostname.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *PTR*               | *target*: Location within the DNS namespace to which this record points.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *TXT*               | *txt*: Arbitrary string data associated with this record.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *HINFO*             | *cpu*: IANA number designating the CPU of the machine referenced by this record. *os*: IANA number designating the Operating System on the machine referenced by this record. See IANA's <a href="http://www.iana.org/assignments/operating-system-names" class="link external">» <em>Operating System Names</em></a> for the meaning of these values.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *SOA*               | *mname*: FQDN of the machine from which the resource records originated. *rname*: Email address of the administrative contain for this domain. *serial*: Serial \# of this revision of the requested domain. *refresh*: Refresh interval (seconds) secondary name servers should use when updating remote copies of this domain. *retry*: Length of time (seconds) to wait after a failed refresh before making a second attempt. *expire*: Maximum length of time (seconds) a secondary DNS server should retain remote copies of the zone data without a successful refresh before discarding. *minimum-ttl*: Minimum length of time (seconds) a client can continue to use a DNS resolution before it should request a new resolution from the server. Can be overridden by individual resource records. |
| *AAAA*              | *ipv6*: IPv6 address                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| *A6*(PHP \>= 5.1.0) | *masklen*: Length (in bits) to inherit from the target specified by `chain`. *ipv6*: Address for this specific record to merge with `chain`. *chain*: Parent record to merge with `ipv6` data.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *SRV*               | *pri*: (Priority) lowest priorities should be used first. *weight*: Ranking to weight which of commonly prioritized `targets` should be chosen at random. *target* and *port*: hostname and port where the requested service can be found. For additional information see: <a href="http://www.faqs.org/rfcs/rfc2782" class="link external">» RFC 2782</a>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *NAPTR*             | *order* and *pref*: Equivalent to `pri` and `weight` above. *flags*, *services*, *regex*, and *replacement*: Parameters as defined by <a href="http://www.faqs.org/rfcs/rfc2915" class="link external">» RFC 2915</a>.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |

### 更新日志

| 版本  | 说明                                                                |
|-------|---------------------------------------------------------------------|
| 5.4.0 | 增加了参数`raw`。                                                   |
| 5.3.0 | 可以是在windows平台上使用这个函数了。                               |
| 5.3.0 | 在此版本之前，如果给参数`authns`传入值，则必须同时传入`addtl`的值。 |

### 范例

**示例 \#1 使用 <span class="function">dns\_get\_record</span>函数**

``` php
<?php
$result = dns_get_record("php.net");
print_r($result);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [host] => php.net
                [type] => MX
                [pri] => 5
                [target] => pair2.php.net
                [class] => IN
                [ttl] => 6765
            )

        [1] => Array
            (
                [host] => php.net
                [type] => A
                [ip] => 64.246.30.37
                [class] => IN
                [ttl] => 8125
            )

    )

**示例 \#2 使用<span
class="function">dns\_get\_record</span>配合DNS\_ANY的例子**

由于我们经常会想获取一个邮件服务器的对应的IP地址的MX记录是否已经生效。在使用<span
class="function">dns\_get\_record</span>函数之后，`addtl`能够返回一个相关的数组记录，`authns`参数则会返回授权服务器的列表信息。

``` php
<?php
/* Request "ANY" record for php.net,
   and create $authns and $addtl arrays
   containing list of name servers and
   any additional records which go with
   them */
$result = dns_get_record("php.net", DNS_ANY, $authns, $addtl);
echo "Result = ";
print_r($result);
echo "Auth NS = ";
print_r($authns);
echo "Additional = ";
print_r($addtl);
?>
```

以上例程的输出类似于：

    Result = Array
    (
        [0] => Array
            (
                [host] => php.net
                [type] => MX
                [pri] => 5
                [target] => pair2.php.net
                [class] => IN
                [ttl] => 6765
            )

        [1] => Array
            (
                [host] => php.net
                [type] => A
                [ip] => 64.246.30.37
                [class] => IN
                [ttl] => 8125
            )

    )
    Auth NS = Array
    (
        [0] => Array
            (
                [host] => php.net
                [type] => NS
                [target] => remote1.easydns.com
                [class] => IN
                [ttl] => 10722
            )

        [1] => Array
            (
                [host] => php.net
                [type] => NS
                [target] => remote2.easydns.com
                [class] => IN
                [ttl] => 10722
            )

        [2] => Array
            (
                [host] => php.net
                [type] => NS
                [target] => ns1.easydns.com
                [class] => IN
                [ttl] => 10722
            )

        [3] => Array
            (
                [host] => php.net
                [type] => NS
                [target] => ns2.easydns.com
                [class] => IN
                [ttl] => 10722
            )

    )
    Additional = Array
    (
        [0] => Array
            (
                [host] => pair2.php.net
                [type] => A
                [ip] => 216.92.131.5
                [class] => IN
                [ttl] => 6766
            )

        [1] => Array
            (
                [host] => remote1.easydns.com
                [type] => A
                [ip] => 64.39.29.212
                [class] => IN
                [ttl] => 100384
            )

        [2] => Array
            (
                [host] => remote2.easydns.com
                [type] => A
                [ip] => 212.100.224.80
                [class] => IN
                [ttl] => 81241
            )

        [3] => Array
            (
                [host] => ns1.easydns.com
                [type] => A
                [ip] => 216.220.40.243
                [class] => IN
                [ttl] => 81241
            )

        [4] => Array
            (
                [host] => ns2.easydns.com
                [type] => A
                [ip] => 216.220.40.244
                [class] => IN
                [ttl] => 81241
            )

    )

### 注释

> **Note**:
>
> For compatibility with versions before PHP 5.3.0 on some operating
> systems, try the
> <a href="https://pear.php.net/" class="link external">» PEAR</a> class
> <a href="https://pear.php.net/package/Net_DNS" class="link external">» Net_DNS</a>.

### 参见

-   <span class="function">dns\_get\_mx</span>
-   <span class="function">dns\_check\_record</span>

fsockopen
=========

打开一个网络连接或者一个Unix套接字连接

### 说明

<span class="type">resource</span> <span
class="methodname">fsockopen</span> ( <span class="methodparam"><span
class="type">string</span> `$hostname`</span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$errno`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$errstr`</span> \[, <span class="methodparam"><span
class="type">float</span> `$timeout`<span class="initializer"> =
ini\_get("default\_socket\_timeout")</span></span> \]\]\]\] )

初始化一个套接字连接到指定主机（`hostname`）。

PHP支持以下的套接字传输器类型列表
<a href="/transports.html" class="xref">所支持的套接字传输器（Socket Transports）列表</a>。也可以通过<span
class="function">stream\_get\_transports</span>来获取套接字传输器支持类型。

默认情况下将以阻塞模式开启套接字连接。当然你可以通过<span
class="function">stream\_set\_blocking</span>将它转换到非阻塞模式。

<span
class="function">stream\_socket\_client</span>与之非常相似，而且提供了更加丰富的参数设置，包括非阻塞模式和提供上下文的的设置。

### 参数

`hostname`  
如果安装了<a href="/openssl/setup.html#安装" class="link">OpenSSL</a>，那么你也许应该在你的主机名地址前面添加访问协议*ssl://*或者是*tls://*，从而可以使用基于TCP/IP协议的SSL或者TLS的客户端连接到远程主机。

`port`  
端口号。如果对该参数传一个-1，则表示不使用端口，例如*unix://*。

`errno`  
如果传入了该参数，holds the system level error number that occurred in
the system-level *connect()* call。

如果`errno`的返回值为*0*，而且这个函数的返回值为**`FALSE`**，那么这表明该错误发生在套接字连接（*connect()*）调用之前，导致连接失败的原因最大的可能是初始化套接字的时候发生了错误。

`errstr`  
错误信息将以字符串的信息返回。

`timeout`  
设置连接的时限，单位为秒。

> **Note**:
>
> 注意：如果你要对建立在套接字基础上的读写操作设置操作时间设置连接时限，请使用<span
> class="function">stream\_set\_timeout</span>，<span
> class="function">fsockopen</span>的连接时限（`timeout`）的参数仅仅在套接字连接的时候生效。

### 返回值

<span
class="function">fsockopen</span>将返回一个文件句柄，之后可以被其他文件类函数调用（例如：<span
class="function">fgets</span>，<span
class="function">fgetss</span>，<span
class="function">fwrite</span>，<span
class="function">fclose</span>还有<span
class="function">feof</span>）。如果调用失败，将返回**`FALSE`**。

### 错误／异常

如果主机（`hostname`）不可访问，将会抛出一个警告级别（**`E_WARNING`**）的错误提示。

### 更新日志

| 版本  | 说明                                                   |
|-------|--------------------------------------------------------|
| 4.3.0 | 在win32系统上增加了对时限设置（`timeout`）参数的支持。 |
| 4.3.0 | 在TCP/IP协议的基础上增加了SSL和TLS。                   |

### 范例

**示例 \#1 <span class="function">fsockopen</span>的例子**

``` php
<?php
$fp = fsockopen("www.example.com", 80, $errno, $errstr, 30);
if (!$fp) {
    echo "$errstr ($errno)<br />\n";
} else {
    $out = "GET / HTTP/1.1\r\n";
    $out .= "Host: www.example.com\r\n";
    $out .= "Connection: Close\r\n\r\n";
    fwrite($fp, $out);
    while (!feof($fp)) {
        echo fgets($fp, 128);
    }
    fclose($fp);
}
?>
```

**示例 \#2 使用UDP连接**

下面这个例子展示了怎么样在自己的机器上通过UDP套接字连接（端口号13）来检索日期和时间。

``` php
<?php
$fp = fsockopen("udp://127.0.0.1", 13, $errno, $errstr);
if (!$fp) {
    echo "ERROR: $errno - $errstr<br />\n";
} else {
    fwrite($fp, "\n");
    echo fread($fp, 26);
    fclose($fp);
}
?>
```

### 注释

> **Note**:
>
> 因为环境的不同，某些情况下在Unix套接字连接或者自定义的连接设置连接时限（`timeout`）可能不会生效。

**Warning**

UDP套接字有些时候在即使远程主机未知的情况，也能打开，并且不发生任何错误。只有当你通过该套接字进行读写的时候才会发现错误。之所以会这样，是因为UDP是一个“非连接状态”的协议，那么这就意味着当前操作系统直到它（套接字）真正需要发送和接受数据的时候才会去尝试为其去建立连接。

> **Note**: <span class="simpara">当指定数值型的 IPv6 地址（例如
> *fe80::1*）时必须用方括号将 IP 围起来——例如，
> *tcp://\[fe80::1\]:80*。</span>

### 参见

-   <span class="function">pfsockopen</span>
-   <span class="function">stream\_socket\_client</span>
-   <span class="function">stream\_set\_blocking</span>
-   <span class="function">stream\_set\_timeout</span>
-   <span class="function">fgets</span>
-   <span class="function">fgetss</span>
-   <span class="function">fwrite</span>
-   <span class="function">fclose</span>
-   <span class="function">feof</span>
-   <span class="function">socket\_connect</span>
-   The <a href="/ref/curl.html" class="link">Curl extension</a>

gethostbyaddr
=============

获取指定的IP地址对应的主机名

### 说明

<span class="type">string</span> <span
class="methodname">gethostbyaddr</span> ( <span
class="methodparam"><span class="type">string</span>
`$ip_address`</span> )

返回指定的IP地址（`ip_address`）对应的主机名。

### 参数

`ip_address`  
主机的IP地址。

### 返回值

成功则返回主机名；失败则原样输出（输出IP地址）；如果输入的格式不正常，则返回**`FALSE`**。

### 范例

**示例 \#1 一个使用 <span class="function">gethostbyaddr</span>
的简单例子**

``` php
<?php
$hostname = gethostbyaddr($_SERVER['REMOTE_ADDR']);

echo $hostname;
?>
```

### 参见

-   <span class="function">gethostbyname</span>
-   <span class="function">gethostbynamel</span>

gethostbyname
=============

返回主机名对应的 IPv4地址。

### 说明

<span class="type">string</span> <span
class="methodname">gethostbyname</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

返回主机名 `hostname` 对应的 IPv4 互联网地址。

### 参数

`hostname`  
主机名

### 返回值

成功时返回 IPv4 地址，失败时原封不动返回 `hostname` 字符串。

### 范例

**示例 \#1 简单的 <span class="function">gethostbyname</span> 例子**

``` php
<?php
$ip = gethostbyname('www.example.com');

echo $ip;
?>
```

### 参见

-   <span class="function">gethostbyaddr</span>
-   <span class="function">gethostbynamel</span>
-   <span class="function">inet\_pton</span>
-   <span class="function">inet\_ntop</span>

gethostbynamel
==============

获取互联网主机名对应的 IPv4 地址列表

### 说明

<span class="type">array</span> <span
class="methodname">gethostbynamel</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

返回互联网主机名 `hostname` 解析出来的 IPv4 地址列表。

### 参数

`hostname`  
主机名。

### 返回值

返回 IPv4 地址数组， 或在 `hostname` 无法解析时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">gethostbynamel</span> 例子**

``` php
<?php
$hosts = gethostbynamel('www.example.com');
print_r($hosts);
?>
```

以上例程会输出：

    Array
    (
        [0] => 192.0.34.166
    )

### 参见

-   <span class="function">gethostbyname</span>
-   <span class="function">gethostbyaddr</span>
-   <span class="function">checkdnsrr</span>
-   <span class="function">getmxrr</span>
-   Linux 手册页 *named(8)*

gethostname
===========

获取主机名

### 说明

<span class="type">string</span> <span
class="methodname">gethostname</span> ( <span
class="methodparam">void</span> )

<span class="function">gethostname</span> 可以获取本地机器的标准主机名。

### 返回值

成功时返回主机名称字符串，失败时返回 **`FALSE`**。

### 范例

**示例 \#1 简单的 <span class="function">gethostname</span> 例子**

``` php
<?php
echo gethostname(); // may output e.g,: sandie

// Or, an option that also works before PHP 5.3
echo php_uname('n'); // may output e.g,: sandie
?>
```

### 参见

-   <span class="function">gethostbyname</span>
-   <span class="function">gethostbyaddr</span>
-   <span class="function">php\_uname</span>

getmxrr
=======

获取互联网主机名对应的 MX 记录

### 说明

<span class="type">bool</span> <span class="methodname">getmxrr</span> (
<span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">array</span> `&$mxhosts`</span> \[, <span
class="methodparam"><span class="type">array</span> `&$weight`</span> \]
)

搜索 `hostname`对应的 MX DNS 记录。

### 参数

`hostname`  
互联网主机名。

`mxhosts`  
找到的 MX 记录列表存放于 `mxhosts` 数组。

`weight`  
提供了 `weight` 数组后，它会用找到的权重信息填充数组。

### 返回值

找到记录返回 **`TRUE`**，没找到或者出错时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                             |
|-------|----------------------------------|
| 5.3.0 | Windows 平台上也能用这个函数了。 |

### 注释

> **Note**:
>
> 本函数不应使用于地址验证。 仅在 MX 记录在 DNS
> 中找到时才会返回，然而根据
> <a href="http://www.faqs.org/rfcs/rfc2821" class="link external">» RFC 2821</a>，
> 没有 MX 记录时， `hostname` 本身就是 MX 主机，优先级为 *0*。

> **Note**:
>
> 在兼容 Windows 实现之前的版本， 可以使用
> <a href="https://pear.php.net/" class="link external">» PEAR</a> class
> 的
> <a href="https://pear.php.net/package/Net_DNS" class="link external">» Net_DNS</a>。

### 参见

-   <span class="function">checkdnsrr</span>
-   <span class="function">dns\_get\_record</span>
-   <span class="function">gethostbyname</span>
-   <span class="function">gethostbynamel</span>
-   <span class="function">gethostbyaddr</span>
-   Linux 手册页面 *named(8)*

getprotobyname
==============

Get protocol number associated with protocol name

### 说明

<span class="type">int</span> <span
class="methodname">getprotobyname</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="function">getprotobyname</span> returns the protocol number
associated with the protocol `name` as per `/etc/protocols`.

### 参数

`name`  
The protocol name.

### 返回值

Returns the protocol number, 或者在失败时返回 **`FALSE`**.

### 范例

**示例 \#1 <span class="function">getprotobyname</span> example**

``` php
<?php
$protocol = 'tcp';
$get_prot = getprotobyname($protocol);
if ($get_prot === FALSE) {
    echo 'Invalid Protocol';
} else {
    echo 'Protocol #' . $get_prot;
}
?>
```

### 参见

-   <span class="function">getprotobynumber</span>

getprotobynumber
================

Get protocol name associated with protocol number

### 说明

<span class="type">string</span> <span
class="methodname">getprotobynumber</span> ( <span
class="methodparam"><span class="type">int</span> `$number`</span> )

<span class="function">getprotobynumber</span> returns the protocol name
associated with protocol `number` as per `/etc/protocols`.

### 参数

`number`  
The protocol number.

### 返回值

Returns the protocol name as a string, 或者在失败时返回 **`FALSE`**.

### 参见

-   <span class="function">getprotobyname</span>

getservbyname
=============

获取互联网服务协议对应的端口

### 说明

<span class="type">int</span> <span
class="methodname">getservbyname</span> ( <span
class="methodparam"><span class="type">string</span> `$service`</span> ,
<span class="methodparam"><span class="type">string</span>
`$protocol`</span> )

<span class="function">getservbyname</span> 返回互联网服务 `service`
指定的协议 `protocol` 中对应的端口， 依据 `/etc/services`。

### 参数

`service`  
互联网服务名称的字符串。

`protocol`  
`protocol` 既可以是 *"tcp"* 也可以是 *"udp"* (小写)。

### 返回值

返回端口号，如果 `service` 或 `protocol` 未找到返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">getservbyname</span> 例子**

``` php
<?php
$services = array('http', 'ftp', 'ssh', 'telnet', 'imap',
'smtp', 'nicname', 'gopher', 'finger', 'pop3', 'www');

foreach ($services as $service) {
    $port = getservbyname($service, 'tcp');
    echo $service . ": " . $port . "<br />\n";
}
?>
```

### 参见

-   <span class="function">getservbyport</span>
-   <a href="http://www.iana.org/assignments/port-numbers" class="link external">» http://www.iana.org/assignments/port-numbers</a>
    端口号的完整列表

getservbyport
=============

Get Internet service which corresponds to port and protocol

### 说明

<span class="type">string</span> <span
class="methodname">getservbyport</span> ( <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span> `$protocol`</span>
)

<span class="function">getservbyport</span> returns the Internet service
associated with `port` for the specified `protocol` as per
`/etc/services`.

### 参数

`port`  
The port number.

`protocol`  
`protocol` is either *"tcp"* or *"udp"* (in lowercase).

### 返回值

Returns the Internet service name as a string.

### 参见

-   <span class="function">getservbyname</span>

header\_register\_callback
==========================

调用一个 header 函数

### 说明

<span class="type">bool</span> <span
class="methodname">header\_register\_callback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

注册一个函数，在 PHP 开始发送输出时调用。

PHP 准备好所有响应头，在发送内容之前执行
`callback`，创建了一个发送响应头的操作窗口。

### 参数

`callback`  
在头发送前调用函数。 它没有参数，返回的值也会被忽略。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">header\_register\_callback</span>
例子**

``` php
<?php

header('Content-Type: text/plain');
header('X-Test: foo');

function foo() {
 foreach (headers_list() as $header) {
   if (strpos($header, 'X-Powered-By:') !== false) {
     header_remove('X-Powered-By');
   }
   header_remove('X-Test');
 }
}

$result = header_register_callback('foo');
echo "a";
?>
```

以上例程的输出类似于：

    Content-Type: text/plain

    a

### 注释

<span class="function">header\_register\_callback</span>
是在头即将发送前执行的， 所以本函数的任意内容输出都会打断输出过程。

> **Note**:
>
> 数据头只会在SAPI支持时得到处理和输出。

### 参见

-   <span class="function">headers\_list</span>
-   <span class="function">header\_remove</span>
-   <span class="function">header</span>

header\_remove
==============

删除之前设置的 HTTP 头

### 说明

<span class="type">void</span> <span
class="methodname">header\_remove</span> (\[ <span
class="methodparam"><span class="type">string</span> `$name`</span> \] )

删除之前用 <span class="function">header</span> 设置的 HTTP 头。

### 参数

`name`  
要移除的头名称。

> **Note**: <span class="simpara"> 参数不分大小写。 </span>

### 返回值

没有返回值。

### 范例

**示例 \#1 取消指定的头**

``` php
<?php
header("X-Foo: Bar");
header("X-Bar: Baz");
header_remove("X-Foo"); 
?>
```

以上例程的输出类似于：

    X-Bar: Baz

**示例 \#2 取消之前全部指定的头**

``` php
<?php
header("X-Foo: Bar");
header("X-Bar: Baz");
header_remove(); 
?>
```

以上例程的输出类似于：

### 注释

**Caution**

本函数会删除*所有* PHP 设置的头， 包括 Cookie、Session 和
*X-Powered-By*。

> **Note**:
>
> 数据头只会在SAPI支持时得到处理和输出。

### 参见

-   <span class="function">header</span>
-   <span class="function">headers\_sent</span>

header
======

发送原生 HTTP 头

### 说明

<span class="type">void</span> <span class="methodname">header</span> (
<span class="methodparam"><span class="type">string</span>
`$string`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$replace`<span class="initializer"> =
true</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$http_response_code`</span> \]\] )

<span class="function">header</span> 用于发送原生的 HTTP 头。关于 HTTP
头的更多信息请参考
<a href="http://www.faqs.org/rfcs/rfc2616" class="link external">» HTTP/1.1 specification</a>。

请注意 <span class="function">header</span>
必须在任何实际输出之前调用，不管是普通的 HTML 标签，还是文件或 PHP
输出的空行，空格。这是个常见的错误，在通过<span
class="function">include</span>，<span
class="function">require</span>，或者其访问其他文件里面的函数的时候，如果在<span
class="function">header</span>被调用之前，其中有空格或者空行。
同样的问题也存在于单独的 PHP/HTML 文件中。

``` php
<html>
<?php
/* This will give an error. Note the output
 * above, which is before the header() call */
header('Location: http://www.example.com/');
exit;
?>
```

### 参数

`string`  
头字符串。

有两种特别的头。第一种以“*HTTP/*”开头的 (case is not
significant)，将会被用来计算出将要发送的HTTP状态码。 例如在 Apache
服务器上用 PHP 脚本来处理不存在文件的请求（使用 *ErrorDocument* 指令），
就会希望脚本响应了正确的状态码。

``` php
<?php
header("HTTP/1.0 404 Not Found");
?>
```

第二种特殊情况是“Location:”的头信息。它不仅把报文发送给浏览器，而且还将返回给浏览器一个
*REDIRECT*（302）的状态码，除非状态码已经事先被设置为了*201*或者*3xx*。

``` php
<?php
header("Location: http://www.example.com/"); /* Redirect browser */

/* Make sure that code below does not get executed when we redirect. */
exit;
?>
```

`replace`  
可选参数 `replace` 表明是否用后面的头替换前面相同类型的头。
默认情况下会替换。如果传入
**`FALSE`**，就可以强制使相同的头信息并存。例如：

``` php
<?php
header('WWW-Authenticate: Negotiate');
header('WWW-Authenticate: NTLM', false);
?>
```

`http_response_code`  
强制指定HTTP响应的值。注意，这个参数只有在报文字符串（`string`）不为空的情况下才有效。

### 返回值

没有返回值。

### 范例

**示例 \#1 下载对话框**

如果你想提醒用户去保存你发送的数据，例如保存一个生成的PDF文件。你可以使用<a href="http://www.faqs.org/rfcs/rfc2183" class="link external">» Content-Disposition</a>的报文信息来提供一个推荐的文件名，并且强制浏览器显示一个文件下载的对话框。

``` php
<?php
// We'll be outputting a PDF
header('Content-type: application/pdf');

// It will be called downloaded.pdf
header('Content-Disposition: attachment; filename="downloaded.pdf"');

// The PDF source is in original.pdf
readfile('original.pdf');
?>
```

**示例 \#2 缓存指令**

PHP脚本总是会生成一些动态内容，而这些内容是不应该被缓存的，不管是客户端浏览器还是在服务器端和客户端浏览器之间的任何代理。我们可以像这样来强制设置浏览器和各个代理层不缓存数据：

``` php
<?php
header("Cache-Control: no-cache, must-revalidate"); // HTTP/1.1
header("Expires: Sat, 26 Jul 1997 05:00:00 GMT"); // Date in the past
?>
```

> **Note**:
>
> 也许你会遇到这样的情况，那就是即使你没使用上面这段代码，你的页面也没有被缓存。大多数情况是因为用户可以自己设置他们的浏览器从而改变浏览器默认的缓存行为。一旦发送了上面这段报文信息，那么你就应该重写那些可能用到缓存了的代码。
>
> 此外，在启用session的情况下，<span
> class="function">session\_cache\_limiter</span>和*session.cache\_limiter*的配置可以用来自动地生成正确的缓存相关的头信息。

### 注释

> **Note**:
>
> 数据头只会在SAPI支持时得到处理和输出。

> **Note**:
>
> 你所有需要输出到浏览器的数据将会一直缓存在服务器端，直到你发送他们，这将造成比较大的资源开销。你可以是用输出缓冲来避开这个问题。你可以通过在脚本里使用<span
> class="function">ob\_start</span>和<span
> class="function">ob\_end\_flush</span>或者直接在你的`php.ini`文件里设置*output\_buffering*，也可以直接在服务器的配置文件里设置。

> **Note**:
>
> HTTP状态信息的报文永远都是最新被发送到客户端的，而不管<span
> class="function">header</span>是否是在最先发送的。报文状态码可能会被重写，当调用<span
> class="function">header</span>来设定新的状态码，除非HTTP报文已经被发送了。

> **Note**:
>
> 在IE 4.01和IE
> 5.5里有bug，要解决就升级浏览器吧，想必也没人用那么远古的神器了吧。

> **Note**: <span
> class="simpara">如果安全模式（<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe mode</a>）被激活，那么脚本的uid将会被添加到*WWW-Authenticate*的*realm*部分，前提是你设置了这个头信息的情况下（使用
> HTTP 认证）。 </span>

> **Note**:
>
> HTTP/1.1需要一个绝对的网络资源地址（URI）来作为一个参数供<a href="http://tools.ietf.org/html/rfc7231-sec14.html#sec14.30" class="link external">» Location:</a>使用，在其中必须包含了协议，主机地址还有完整的路径，但是一些客户端可以接受相对的网络资源地址。你可以在一个相对的网路资源地址的基础上使用`$_SERVER['HTTP_HOST']`，`$_SERVER['PHP_SELF']`和<span
> class="function">dirname</span>来组装一个绝对的网路资源地址。
>
> ``` php
> <?php
> /* Redirect to a different page in the current directory that was requested */
> $host  = $_SERVER['HTTP_HOST'];
> $uri   = rtrim(dirname($_SERVER['PHP_SELF']), '/\\');
> $extra = 'mypage.php';
> header("Location: http://$host$uri/$extra");
> exit;
> ?>
> ```

> **Note**:
>
> 在执行Location header跳转的时候，Session
> ID无法通传递的，即使<a href="/session/setup.html#" class="link">session.use_trans_sid</a>是激活状态的。只能通过手动传递using
> **`SID`**的值来实现。

### 参见

-   <span class="function">headers\_sent</span>
-   <span class="function">setcookie</span>
-   <span class="function">http\_response\_code</span>
-   The section on
    <a href="/features/http-auth.html" class="link">HTTP authentication</a>

headers\_list
=============

返回已发送的 HTTP 响应头（或准备发送的）

### 说明

<span class="type">array</span> <span
class="methodname">headers\_list</span> ( <span
class="methodparam">void</span> )

<span class="function">headers\_list</span>
会返回准备发送给浏览器/客户端的 HTTP 头列表。
检测这些头是否已经发送，使用 <span
class="function">headers\_sent</span>。

### 返回值

返回数字索引的头数组。

### 范例

**示例 \#1 使用 <span class="function">headers\_list</span> 的例子**

``` php
<?php

/* setcookie() 会自己添加一个响应头 */
setcookie('foo', 'bar');

/* 添加自定义的响应头
 大多数客户端会主动忽略 */
header("X-Sample-Test: foo");

/* 响应中指定内容为明文 text */
header('Content-type: text/plain');

/* 所以会发送什么头呢？ */
var_dump(headers_list());

?>
```

以上例程会输出：

    array(4) {
      [0]=>
      string(23) "X-Powered-By: PHP/5.1.3"
      [1]=>
      string(19) "Set-Cookie: foo=bar"
      [2]=>
      string(18) "X-Sample-Test: foo"
      [3]=>
      string(24) "Content-type: text/plain"
    }

### 注释

> **Note**:
>
> 数据头只会在SAPI支持时得到处理和输出。

### 参见

-   <span class="function">headers\_sent</span>
-   <span class="function">header</span>
-   <span class="function">setcookie</span>
-   <span class="function">apache\_response\_headers</span>
-   <span class="function">http\_response\_code</span>

headers\_sent
=============

检测 HTTP 头是否已经发送

### 说明

<span class="type">bool</span> <span
class="methodname">headers\_sent</span> (\[ <span
class="methodparam"><span class="type">string</span> `&$file`</span> \[,
<span class="methodparam"><span class="type">int</span> `&$line`</span>
\]\] )

检测 HTTP 头是否已经发送。

HTTP 头已经发送时，就无法通过 <span class="function">header</span>
添加更多头字段。 使用此函数起码可以防止 HTTP 头出错。另一个解决方案是用
<a href="/ref/outcontrol.html" class="link">输出缓冲</a>。

### 参数

`file`  
若设置了可选参数 `file` and `line`， <span
class="function">headers\_sent</span> 会把 PHP 文件名放在 `file`
变量里， 输出开始的行号放在 `line` 变量里。

`line`  
输出开始的行号。

### 返回值

HTTP 头未发送时，<span class="function">headers\_sent</span> 返回
**`FALSE`**，否则返回 **`TRUE`**。

### 范例

**示例 \#1 使用 <span class="function">headers\_sent</span> 的例子**

``` php
<?php

// 没有 HTTP 头就发送一个
if (!headers_sent()) {
    header('Location: http://www.example.com/');
    exit;
}

// 使用 file 和 line 参数选项的例子
// 注意 $filename 和 $linenum 用于下文中使用
// 所以不要提前为它们赋值
if (!headers_sent($filename, $linenum)) {
    header('Location: http://www.example.com/');
    exit;

// 很有可能在这里触发错误
} else {

    echo "Headers already sent in $filename on line $linenum\n" .
          "Cannot redirect, for now please click this <a " .
          "href=\"http://www.example.com\">link</a> instead\n";
    exit;
}

?>
```

### 注释

> **Note**:
>
> 数据头只会在SAPI支持时得到处理和输出。

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">trigger\_error</span>
-   <span class="function">headers\_list</span>
-   <span class="function">header</span> 中有更多相关细节的讨论。

http\_response\_code
====================

获取/设置响应的 HTTP 状态码

### 说明

<span class="type">mixed</span> <span
class="methodname">http\_response\_code</span> (\[ <span
class="methodparam"><span class="type">int</span>
`$response_code`</span> \] )

获取或者设置响应的 HTTP 状态码。

### 参数

`response_code`  
可选的 `response_code` 会设置响应的状态码。

### 返回值

如果提供了 `response_code`，将返回先前的状态码。 如果未提供
`response_code`，会返回当前的状态码。 在 Web
服务器环境里，这些状态码的默认值都是 *200*。

如果在非 Web 服务器环境里调用（比如 CLI 应用里）， 不提供
`response_code` 就会返回 **`FALSE`** 。 在非 Web 服务器环境里，提供
`response_code` 会返回 **`TRUE`** （仅仅在先前没有设置过状态码的时候）。

### 范例

**示例 \#1 Web 服务器环境内使用 <span
class="function">http\_response\_code</span>**

``` php
<?php

// 获取当前状态码，并设置新的状态码
var_dump(http_response_code(404));

//获取新的状态码
var_dump(http_response_code());
?>
```

以上例程会输出：

    int(200)
    int(404)

**示例 \#2 在 CLI 环境内使用 <span
class="function">http\_response\_code</span>**

``` php
<?php

// 获取当前默认的响应状态码 
var_dump(http_response_code());

// 设置状态码
var_dump(http_response_code(201));

// 获取新的状态码
var_dump(http_response_code());
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    int(201)

### 参见

-   <span class="function">header</span>
-   <span class="function">headers\_list</span>

inet\_ntop
==========

Converts a packed internet address to a human readable representation

### 说明

<span class="type">string</span> <span
class="methodname">inet\_ntop</span> ( <span class="methodparam"><span
class="type">string</span> `$in_addr`</span> )

This function converts a 32bit IPv4, or 128bit IPv6 address (if PHP was
built with IPv6 support enabled) into an address family appropriate
string representation.

### 参数

`in_addr`  
A 32bit IPv4, or 128bit IPv6 address.

### 返回值

Returns a string representation of the address 或者在失败时返回
**`FALSE`**.

### 范例

**示例 \#1 <span class="function">inet\_ntop</span> Example**

``` php
<?php
$packed = chr(127) . chr(0) . chr(0) . chr(1);
$expanded = inet_ntop($packed);

/* Outputs: 127.0.0.1 */
echo $expanded;

$packed = str_repeat(chr(0), 15) . chr(1);
$expanded = inet_ntop($packed);

/* Outputs: ::1 */
echo $expanded;
?>
```

### 参见

-   <span class="function">long2ip</span>
-   <span class="function">ip2long</span>
-   <span class="function">inet\_pton</span>

inet\_pton
==========

Converts a human readable IP address to its packed in\_addr
representation

### 说明

<span class="type">string</span> <span
class="methodname">inet\_pton</span> ( <span class="methodparam"><span
class="type">string</span> `$address`</span> )

This function converts a human readable IPv4 or IPv6 address (if PHP was
built with IPv6 support enabled) into an address family appropriate
32bit or 128bit binary structure.

### 参数

`address`  
A human readable IPv4 or IPv6 address.

### 返回值

Returns the *in\_addr* representation of the given `address`, or
**`FALSE`** if a syntactically invalid `address` is given (for example,
an IPv4 address without dots or an IPv6 address without colons).

### 范例

**示例 \#1 <span class="function">inet\_pton</span> Example**

``` php
<?php
$in_addr = inet_pton('127.0.0.1');
 
$in6_addr = inet_pton('::1');
?>
```

### 参见

-   <span class="function">ip2long</span>
-   <span class="function">long2ip</span>
-   <span class="function">inet\_ntop</span>

ip2long
=======

将 IPV4 的字符串互联网协议转换成长整型数字

### 说明

<span class="type">int</span> <span class="methodname">ip2long</span> (
<span class="methodparam"><span class="type">string</span>
`$ip_address`</span> )

函数 <span class="function">ip2long</span> 返回 IPV4
网络地址的长整型格式，从标准网络地址格式(点字符串)转化得到。

<span class="function">ip2long</span> 还可以与非完整IP进行工作。 阅读
<a href="http://publibn.boulder.ibm.com/doc_link/en_US/a_doc_lib/libs/commtrf2/inet_addr.htm" class="link external">» http://publibn.boulder.ibm.com/doc_link/en_US/a_doc_lib/libs/commtrf2/inet_addr.htm</a>
获得更多信息。

### 参数

`ip_address`  
一个标准格式的地址。

### 返回值

返回IP地址转换后的数字 或 **`FALSE`** 如果 `ip_address` 是无效的。

### 更新日志

| 版本   | 说明                                                                                                                                                                                           |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.5.0  | Prior to this version, on Windows <span class="function">ip2long</span> would sometimes return a valid number even if passed a value which was not an (IPv4) Internet Protocol dotted address. |
| 5.2.10 | 再此之前的版本, <span class="function">ip2long</span> 有时会返回即使这不是一个IPV4的标准地址的数字地址。                                                                                       |

### 范例

**示例 \#1 <span class="function">ip2long</span> 例子**

``` php
<?php
$ip = gethostbyname('www.example.com');
$out = "The following URLs are equivalent:<br />\n";
$out .= 'http://www.example.com/, http://' . $ip . '/, and http://' . sprintf("%u", ip2long($ip)) . "/<br />\n";
echo $out;
?>
```

**示例 \#2 显示IP地址**

第二个例子说明打印一个转换后的地址使用 <span
class="function">printf</span> 在PHP4和PHP5的功能:

``` php
<?php
$ip   = gethostbyname('www.example.com');
$long = ip2long($ip);

if ($long == -1 || $long === FALSE) {
    echo 'Invalid IP, please try again';
} else {
    echo $ip   . "\n";           // 192.0.34.166
    echo $long . "\n";           // -1073732954
    printf("%u\n", ip2long($ip)); // 3221234342
}
?>
```

### 注释

> **Note**:
>
> 因为PHP的 <span class="type">integer</span>
> 类型是有符号，并且有许多的IP地址讲导致在32位系统的情况下为负数，
> 你需要使用 "%u" 进行转换通过 <span class="function">sprintf</span> 或
> <span class="function">printf</span>
> 得到的字符串来表示无符号的IP地址。

> **Note**:
>
> <span class="function">ip2long</span> 将返回 **`FALSE`** 在IP是
> *255.255.255.255* 的情况，版本为 PHP 5 \<= 5.0.2. 在修复后 PHP 5.0.3
> 会返回 *-1* (与PHP4相同).

### 参见

-   <span class="function">long2ip</span>
-   <span class="function">sprintf</span>

long2ip
=======

将长整型转化为字符串形式带点的互联网标准格式地址（IPV4）

### 说明

<span class="type">string</span> <span class="methodname">long2ip</span>
( <span class="methodparam"><span class="type">int</span>
`$proper_address`</span> )

<span class="function">long2ip</span>
函数通过长整型的表达形式转化生成带点格式的互联网地址（例如：aaa.bbb.ccc.ddd
）。

### 参数

`proper_address`  
合格的地址，长整型的表达形式。

### 返回值

返回字符串的互联网 IP 地址。

### 更新日志

| 版本  | 说明                                                                                                     |
|-------|----------------------------------------------------------------------------------------------------------|
| 7.1.0 | 参数 `proper_address` 的类型从 <span class="type">string</span> 改成 <span class="type">integer</span>。 |

### 注释

> **Note**:
>
> 在 32 位架构中，从 <span class="type">string</span> 转换 <span
> class="type">integer</span> 整型形式的 ip
> 地址将有可能导致错误的结果，因为结果数字超出了 **`PHP_INT_MAX`**
> 限制。

### 参见

-   <span class="function">ip2long</span>

openlog
=======

Open connection to system logger

### 说明

<span class="type">bool</span> <span class="methodname">openlog</span> (
<span class="methodparam"><span class="type">string</span>
`$ident`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> , <span
class="methodparam"><span class="type">int</span> `$facility`</span> )

<span class="function">openlog</span> opens a connection to the system
logger for a program.

The use of <span class="function">openlog</span> is optional. It will
automatically be called by <span class="function">syslog</span> if
necessary, in which case `ident` will default to **`FALSE`**.

### 参数

`ident`  
The string `ident` is added to each message.

`option`  
The `option` argument is used to indicate what logging options will be
used when generating a log message.

| Constant         | Description                                                                                        |
|------------------|----------------------------------------------------------------------------------------------------|
| **`LOG_CONS`**   | if there is an error while sending data to the system logger, write directly to the system console |
| **`LOG_NDELAY`** | open the connection to the logger immediately                                                      |
| **`LOG_ODELAY`** | (default) delay opening the connection until the first message is logged                           |
| **`LOG_PERROR`** | print log message also to standard error                                                           |
| **`LOG_PID`**    | include PID with each message                                                                      |

You can use one or more of these options. When using multiple options
you need to *OR* them, i.e. to open the connection immediately, write to
the console and include the PID in each message, you will use:
*LOG\_CONS \| LOG\_NDELAY \| LOG\_PID*

`facility`  
The `facility` argument is used to specify what type of program is
logging the message. This allows you to specify (in your machine's
syslog configuration) how messages coming from different facilities will
be handled.

| Constant                              | Description                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------|
| **`LOG_AUTH`**                        | security/authorization messages (use **`LOG_AUTHPRIV`** instead in systems where that constant is defined) |
| **`LOG_AUTHPRIV`**                    | security/authorization messages (private)                                                                  |
| **`LOG_CRON`**                        | clock daemon (cron and at)                                                                                 |
| **`LOG_DAEMON`**                      | other system daemons                                                                                       |
| **`LOG_KERN`**                        | kernel messages                                                                                            |
| **`LOG_LOCAL0`** ... **`LOG_LOCAL7`** | reserved for local use, these are not available in Windows                                                 |
| **`LOG_LPR`**                         | line printer subsystem                                                                                     |
| **`LOG_MAIL`**                        | mail subsystem                                                                                             |
| **`LOG_NEWS`**                        | USENET news subsystem                                                                                      |
| **`LOG_SYSLOG`**                      | messages generated internally by syslogd                                                                   |
| **`LOG_USER`**                        | generic user-level messages                                                                                |
| **`LOG_UUCP`**                        | UUCP subsystem                                                                                             |

> **Note**:
>
> **`LOG_USER`** is the only valid log type under Windows operating
> systems

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">syslog</span>
-   <span class="function">closelog</span>

pfsockopen
==========

打开一个持久的网络连接或者Unix套接字连接。

### 说明

<span class="type">resource</span> <span
class="methodname">pfsockopen</span> ( <span class="methodparam"><span
class="type">string</span> `$hostname`</span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = -1</span></span> \[, <span
class="methodparam"><span class="type">int</span> `&$errno`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$errstr`</span> \[, <span class="methodparam"><span
class="type">float</span> `$timeout`<span class="initializer"> =
ini\_get("default\_socket\_timeout")</span></span> \]\]\]\] )

这个函数的作用与<span
class="function">fsockopen</span>完全一样的，不同的地方在于当在脚本执行完后，连接一直不会关闭。可以说它是<span
class="function">fsockopen</span>的长连接版本。

### 参数

对于其参数的信息，请参考<span class="function">fsockopen</span>的文档。

### 参见

-   <span class="function">fsockopen</span>

setcookie
=========

发送 Cookie

### 说明

<span class="type">bool</span> <span class="methodname">setcookie</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">string</span> `$value`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$expire`<span class="initializer"> =
0</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$path`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">string</span> `$domain`<span class="initializer"> =
""</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$secure`<span class="initializer"> =
false</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$httponly`<span class="initializer"> =
false</span></span> \]\]\]\]\]\] )

<span class="function">setcookie</span> 定义了 Cookie，会和剩下的 HTTP
头一起发送给客户端。 和其他 HTTP
头一样，必须在脚本产生任意输出*之前*发送 Cookie（由于协议的限制）。
请在产生任何输出之前（包括 *\<html\>* 和 *\<head\>*
或者空格）调用本函数。

一旦设置 Cookie 后，下次打开页面时可以使用 `$_COOKIE` 读取。 Cookie
值同样也存在于 `$_REQUEST`。

### 参数

<a href="http://www.faqs.org/rfcs/rfc6265" class="link external">» RFC 6265</a>
提供了 <span class="function">setcookie</span> 每个参数的参考标准。

`name`  
Cookie 名称。

`value`  
Cookie 值。 这个值储存于用户的电脑里，请勿储存敏感信息。 比如 `name` 是
*'cookiename'*， 可通过 `$_COOKIE['cookiename']` 获取它的值。

`expire`  
Cookie 的过期时间。 这是个 Unix 时间戳，即 Unix 纪元以来（格林威治时间
1970 年 1 月 1 日 00:00:00）的秒数。 也就是说，基本可以用 <span
class="function">time</span> 函数的结果加上希望过期的秒数。 或者也可以用
<span class="function">mktime</span>。 *time()+60\*60\*24\*30* 就是设置
Cookie 30 天后过期。 如果设置成零，或者忽略参数， Cookie
会在会话结束时过期（也就是关掉浏览器时）。

> **Note**:
>
> 你可能注意到了，`expire` 使用 Unix 时间戳而非 *Wdy, DD-Mon-YYYY
> HH:MM:SS GMT* 这样的日期格式，是因为 PHP 内部作了转换。

`path`  
Cookie 有效的服务器路径。 设置成 *'/'* 时，Cookie 对整个域名 `domain`
有效。 如果设置成 *'/foo/'*， Cookie 仅仅对 `domain` 中 */foo/*
目录及其子目录有效（比如 */foo/bar/*）。 默认值是设置 Cookie
时的当前目录。

`domain`  
Cookie 的有效域名/子域名。 设置成子域名（例如
*'www.example.com'*），会使 Cookie 对这个子域名和它的三级域名有效（例如
w2.www.example.com）。 要让 Cookie
对整个域名有效（包括它的全部子域名），只要设置成域名就可以了（这个例子里是
*'example.com'*）。

旧版浏览器仍然在使用废弃的
<a href="http://www.faqs.org/rfcs/rfc2109" class="link external">» RFC 2109</a>，
需要一个前置的点 *.* 来匹配所有子域名。

`secure`  
设置这个 Cookie 是否仅仅通过安全的 HTTPS 连接传给客户端。 设置成
**`TRUE`** 时，只有安全连接存在时才会设置 Cookie。
如果是在服务器端处理这个需求，程序员需要仅仅在安全连接上发送此类 Cookie
（通过 `$_SERVER["HTTPS"]` 判断）。

`httponly`  
设置成 **`TRUE`**，Cookie 仅可通过 HTTP 协议访问。 这意思就是 Cookie
无法通过类似 JavaScript 这样的脚本语言访问。 要有效减少 XSS
攻击时的身份窃取行为，可建议用此设置（虽然不是所有浏览器都支持），不过这个说法经常有争议。
PHP 5.2.0 中添加。 **`TRUE`** 或 **`FALSE`**

### 返回值

如果在调用本函数以前就产生了输出，<span
class="function">setcookie</span> 会调用失败并返回 **`FALSE`**。 如果
<span class="function">setcookie</span> 成功运行，返回
**`TRUE`**。当然，它的意思并非用户是否已接受 Cookie。

### 范例

发送 Cookie 的几个例子：

**示例 \#1 <span class="function">setcookie</span> 发送例子**

``` php
<?php
$value = 'something from somewhere';

setcookie("TestCookie", $value);
setcookie("TestCookie", $value, time()+3600);  /* 1 小时过期  */
setcookie("TestCookie", $value, time()+3600, "/~rasmus/", "example.com", 1);
?>
```

注意：在发送 Cookie 时，值的部分会被自动 urlencode 编码。收到 Cookie
时，会自动解码，并赋值到可变的 Cookie 名称上。 如果不想被编码，可以使用
<span class="function">setrawcookie</span> 代替——如果你的 PHP 版本是 5
及以上。 在脚本里查看我们的测试 Cookie 的内容，使用下面的一个例子：

``` php
<?php
// 打印一个单独的 Cookie
echo $_COOKIE["TestCookie"];

//  debug/test 查看所有 Cookie 的另一种方式
print_r($_COOKIE);
?>
```

**示例 \#2 <span class="function">setcookie</span> 删除例子**

要删除一个 Cookie，应该设置过期时间为过去，以触发浏览器的删除机制。
下面的例子展示了如何删除上个例子里的 Cookie：

``` php
<?php
// 设置过期时间为一个小时前
setcookie("TestCookie", "", time() - 3600);
setcookie("TestCookie", "", time() - 3600, "/~rasmus/", "example.com", 1);
?>
```

**示例 \#3 <span class="function">setcookie</span> 和数组**

通过带 array 标记的 Cookie 名称，也可以把 Cookie 设置成数组。
如果有数组元素，可以把它放进 Cookie 里； 脚本接收到时，Cookie
名称里的值会是一个数组：

``` php
<?php
// 设置 Cookie
setcookie("cookie[three]", "cookiethree");
setcookie("cookie[two]", "cookietwo");
setcookie("cookie[one]", "cookieone");

// 网页刷新后，打印出以下内容
if (isset($_COOKIE['cookie'])) {
    foreach ($_COOKIE['cookie'] as $name => $value) {
        $name = htmlspecialchars($name);
        $value = htmlspecialchars($value);
        echo "$name : $value <br />\n";
    }
}
?>
```

以上例程会输出：

    three : cookiethree
    two : cookietwo
    one : cookieone

### 更新日志

| 版本  | 说明                                                  |
|-------|-------------------------------------------------------|
| 5.5.0 | 发送给客户端的 Set-Cookie 头现在会包含 Max-Age 属性。 |
| 5.2.0 | 添加 `httponly` 参数。                                |

### 注释

> **Note**:
>
> 要在调用本函数前输出内容，可以使用输出缓冲：让输出的内容在服务器里缓冲起来，
> 直至真正发送给浏览器。 可在脚本里调用 <span
> class="function">ob\_start</span> 和 <span
> class="function">ob\_end\_flush</span>， 或设置 *output\_buffering*
> `php.ini` 或服务器配置文件里的配置指令。

> **Note**:
>
> 如果 PHP 指令
> <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
> 设置成 *on*，Cookie 值会自动设置成变量。 下面的例子里会存在
> `$TestCookie`。 我们推荐你使用 `$_COOKIE`。

注意避坑：

-   <span class="simpara"> 在页面（ Cookie
    可见的页面）下次刷新前，Cookie 不会生效。 测试 Cookie
    是否已经成功设置，需要在下次页面加载时、Cookie 过期前检测。
    过期时间是通过 `expire` 参数设置的。 直接调用 *print\_r($\_COOKIE);*
    调试检测 Cookie 是个很好的方式。 </span>
-   <span class="simpara"> 为同一个参数再次设置 Cookie
    前，必须先把它删掉。 如果参数的值是空 string 或
    **`FALSE`**，并且其他参数和上次调用 setcookie 仍旧一样，
    则指定的名称会被远程客户端删除。 内部的实现是：将值设置成
    'deleted'，并且过期时间是一年前。 </span>
-   <span class="simpara"> 因为设置值成 **`FALSE`** 会导致 Cookie
    被删除，所以要避免使用布尔值。 代替方式：*0* 是 **`FALSE`**，*1* 是
    **`TRUE`**。 </span>
-   <span class="simpara"> Cookie 名称可以设置成数组名称，PHP
    脚本里会是数组， 但用户系统里储存的是单独分开的 Cookie。
    可以考虑使用 <span class="function">explode</span> 为一个 Cookie
    设置多个名称和值。 不建议将 <span class="function">serialize</span>
    用于此处，因为它会导致安全漏洞。 </span>

多次调用 <span class="function">setcookie</span> 会按调用顺序执行。

### 参见

-   <span class="function">header</span>
-   <span class="function">setrawcookie</span>
-   <a href="/features/cookies.html" class="link">Cookie 章节</a>
-   <a href="http://www.faqs.org/rfcs/rfc6265" class="link external">» RFC 6265</a>
-   <a href="http://www.faqs.org/rfcs/rfc2109" class="link external">» RFC 2109</a>

setrawcookie
============

发送未经 URL 编码的 cookie

### 说明

<span class="type">bool</span> <span
class="methodname">setrawcookie</span> ( <span class="methodparam"><span
class="type">string</span> `$name`</span> \[, <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$expire`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$domain`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$secure`<span class="initializer"> =
false</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$httponly`<span class="initializer"> =
false</span></span> \]\]\]\]\]\] )

<span class="function">setrawcookie</span> 和 <span
class="function">setcookie</span> 非常相似，唯一不同之处是发送到浏览器的
cookie 值没有自动经过 URL 编码（urlencode）。

### 参数

相关参数的信息参见 <span class="function">setcookie</span> 的文档。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                  |
|-------|-------------------------------------------------------|
| 5.5.0 | 发送给客户端的 Set-Cookie 头现在会加上 Max-Age 属性。 |
| 5.2.0 | 增加了 `httponly` 参数。                              |

### 参见

-   <span class="function">setcookie</span>

socket\_get\_status
===================

别名 <span class="function">stream\_get\_meta\_data</span>

### 说明

此函数是该函数的别名： <span
class="function">stream\_get\_meta\_data</span>。

socket\_set\_blocking
=====================

别名 <span class="function">stream\_set\_blocking</span>

### 说明

此函数是该函数的别名： <span
class="function">stream\_set\_blocking</span>。

socket\_set\_timeout
====================

别名 <span class="function">stream\_set\_timeout</span>

### 说明

此函数是该函数的别名： <span
class="function">stream\_set\_timeout</span>。

syslog
======

Generate a system log message

### 说明

<span class="type">bool</span> <span class="methodname">syslog</span> (
<span class="methodparam"><span class="type">int</span>
`$priority`</span> , <span class="methodparam"><span
class="type">string</span> `$message`</span> )

<span class="function">syslog</span> generates a log message that will
be distributed by the system logger.

For information on setting up a user defined log handler, see the <span
class="citerefentry"><span class="refentrytitle">syslog.conf</span>
<span class="manvolnum">(5)</span></span> Unix manual page. More
information on the syslog facilities and option can be found in the man
pages for <span class="citerefentry"><span
class="refentrytitle">syslog</span> <span
class="manvolnum">(3)</span></span> on Unix machines.

### 参数

`priority`  
`priority` is a combination of the facility and the level. Possible
values are:

| Constant          | Description                        |
|-------------------|------------------------------------|
| **`LOG_EMERG`**   | system is unusable                 |
| **`LOG_ALERT`**   | action must be taken immediately   |
| **`LOG_CRIT`**    | critical conditions                |
| **`LOG_ERR`**     | error conditions                   |
| **`LOG_WARNING`** | warning conditions                 |
| **`LOG_NOTICE`**  | normal, but significant, condition |
| **`LOG_INFO`**    | informational message              |
| **`LOG_DEBUG`**   | debug-level message                |

`message`  
The message to send, except that the two characters *%m* will be
replaced by the error message string (strerror) corresponding to the
present value of <span class="errortype">errno</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Using <span class="function">syslog</span>**

``` php
<?php
// open syslog, include the process ID and also send
// the log to standard error, and use a user defined
// logging mechanism
openlog("myScriptLog", LOG_PID | LOG_PERROR, LOG_LOCAL0);

// some code

if (authorized_client()) {
    // do something
} else {
    // unauthorized client!
    // log the attempt
    $access = date("Y/m/d H:i:s");
    syslog(LOG_WARNING, "Unauthorized client: $access {$_SERVER['REMOTE_ADDR']} ({$_SERVER['HTTP_USER_AGENT']})");
}

closelog();
?>
```

### 注释

On Windows NT, the syslog service is emulated using the Event Log.

> **Note**:
>
> Use of *LOG\_LOCAL0* through *LOG\_LOCAL7* for the `facility`
> parameter of <span class="function">openlog</span> is not available in
> Windows.

### 参见

-   <span class="function">openlog</span>
-   <span class="function">closelog</span>

**目录**

-   [checkdnsrr](/ref/network.html#checkdnsrr) —
    给指定的主机（域名）或者IP地址做DNS通信检查
-   [closelog](/ref/network.html#closelog) — 关闭系统日志链接
-   [define\_syslog\_variables](/ref/network.html#define_syslog_variables)
    — Initializes all syslog related variables
-   [dns\_check\_record](/ref/network.html#dns_check_record) — 别名
    checkdnsrr
-   [dns\_get\_mx](/ref/network.html#dns_get_mx) — 别名 getmxrr
-   [dns\_get\_record](/ref/network.html#dns_get_record) —
    获取指定主机的DNS记录
-   [fsockopen](/ref/network.html#fsockopen) —
    打开一个网络连接或者一个Unix套接字连接
-   [gethostbyaddr](/ref/network.html#gethostbyaddr) —
    获取指定的IP地址对应的主机名
-   [gethostbyname](/ref/network.html#gethostbyname) — 返回主机名对应的
    IPv4地址。
-   [gethostbynamel](/ref/network.html#gethostbynamel) —
    获取互联网主机名对应的 IPv4 地址列表
-   [gethostname](/ref/network.html#gethostname) — 获取主机名
-   [getmxrr](/ref/network.html#getmxrr) — 获取互联网主机名对应的 MX
    记录
-   [getprotobyname](/ref/network.html#getprotobyname) — Get protocol
    number associated with protocol name
-   [getprotobynumber](/ref/network.html#getprotobynumber) — Get
    protocol name associated with protocol number
-   [getservbyname](/ref/network.html#getservbyname) —
    获取互联网服务协议对应的端口
-   [getservbyport](/ref/network.html#getservbyport) — Get Internet
    service which corresponds to port and protocol
-   [header\_register\_callback](/ref/network.html#header_register_callback)
    — 调用一个 header 函数
-   [header\_remove](/ref/network.html#header_remove) — 删除之前设置的
    HTTP 头
-   [header](/ref/network.html#header) — 发送原生 HTTP 头
-   [headers\_list](/ref/network.html#headers_list) — 返回已发送的 HTTP
    响应头（或准备发送的）
-   [headers\_sent](/ref/network.html#headers_sent) — 检测 HTTP
    头是否已经发送
-   [http\_response\_code](/ref/network.html#http_response_code) —
    获取/设置响应的 HTTP 状态码
-   [inet\_ntop](/ref/network.html#inet_ntop) — Converts a packed
    internet address to a human readable representation
-   [inet\_pton](/ref/network.html#inet_pton) — Converts a human
    readable IP address to its packed in\_addr representation
-   [ip2long](/ref/network.html#ip2long) — 将 IPV4
    的字符串互联网协议转换成长整型数字
-   [long2ip](/ref/network.html#long2ip) —
    将长整型转化为字符串形式带点的互联网标准格式地址（IPV4）
-   [openlog](/ref/network.html#openlog) — Open connection to system
    logger
-   [pfsockopen](/ref/network.html#pfsockopen) —
    打开一个持久的网络连接或者Unix套接字连接。
-   [setcookie](/ref/network.html#setcookie) — 发送 Cookie
-   [setrawcookie](/ref/network.html#setrawcookie) — 发送未经 URL 编码的
    cookie
-   [socket\_get\_status](/ref/network.html#socket_get_status) — 别名
    stream\_get\_meta\_data
-   [socket\_set\_blocking](/ref/network.html#socket_set_blocking) —
    别名 stream\_set\_blocking
-   [socket\_set\_timeout](/ref/network.html#socket_set_timeout) — 别名
    stream\_set\_timeout
-   [syslog](/ref/network.html#syslog) — Generate a system log message
