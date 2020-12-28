SNMP
====

**目录**

-   [简介](/intro/snmp.html)
-   [安装／配置](/snmp/setup.html)
    -   [需求](/snmp/setup.html#需求)
    -   [安装](/snmp/setup.html#安装)
    -   [运行时配置](/snmp/setup.html#运行时配置)
    -   [资源类型](/snmp/setup.html#资源类型)
-   [预定义常量](/snmp/constants.html)
-   [SNMP 函数](/ref/snmp.html)
    -   [snmp\_get\_quick\_print](/ref/snmp.html#snmp_get_quick_print) —
        返回 UCD 库中 quick\_print 设置的当前值
    -   [snmp\_get\_valueretrieval](/ref/snmp.html#snmp_get_valueretrieval)
        — Return the method how the SNMP values will be returned
    -   [snmp\_read\_mib](/ref/snmp.html#snmp_read_mib) — Reads and
        parses a MIB file into the active MIB tree
    -   [snmp\_set\_enum\_print](/ref/snmp.html#snmp_set_enum_print) —
        Return all values that are enums with their enum value instead
        of the raw integer
    -   [snmp\_set\_oid\_numeric\_print](/ref/snmp.html#snmp_set_oid_numeric_print)
        — Set the OID output format
    -   [snmp\_set\_oid\_output\_format](/ref/snmp.html#snmp_set_oid_output_format)
        — Set the OID output format
    -   [snmp\_set\_quick\_print](/ref/snmp.html#snmp_set_quick_print) —
        设置 UCD SNMP 库中 quick\_print 的值
    -   [snmp\_set\_valueretrieval](/ref/snmp.html#snmp_set_valueretrieval)
        — Specify the method how the SNMP values will be returned
    -   [snmp2\_get](/ref/snmp.html#snmp2_get) — Fetch an SNMP object
    -   [snmp2\_getnext](/ref/snmp.html#snmp2_getnext) — Fetch the SNMP
        object which follows the given object id
    -   [snmp2\_real\_walk](/ref/snmp.html#snmp2_real_walk) — Return all
        objects including their respective object ID within the
        specified one
    -   [snmp2\_set](/ref/snmp.html#snmp2_set) — Set the value of an
        SNMP object
    -   [snmp2\_walk](/ref/snmp.html#snmp2_walk) — Fetch all the SNMP
        objects from an agent
    -   [snmp3\_get](/ref/snmp.html#snmp3_get) — Fetch an SNMP object
    -   [snmp3\_getnext](/ref/snmp.html#snmp3_getnext) — Fetch the SNMP
        object which follows the given object id
    -   [snmp3\_real\_walk](/ref/snmp.html#snmp3_real_walk) — Return all
        objects including their respective object ID within the
        specified one
    -   [snmp3\_set](/ref/snmp.html#snmp3_set) — Set the value of an
        SNMP object
    -   [snmp3\_walk](/ref/snmp.html#snmp3_walk) — Fetch all the SNMP
        objects from an agent
    -   [snmpget](/ref/snmp.html#snmpget) — 获取一个 SNMP 对象
    -   [snmpgetnext](/ref/snmp.html#snmpgetnext) — Fetch the SNMP
        object which follows the given object id
    -   [snmprealwalk](/ref/snmp.html#snmprealwalk) —
        返回指定的所有对象，包括它们各自的对象 ID
    -   [snmpset](/ref/snmp.html#snmpset) — 设置一个 SNMP 对象
    -   [snmpwalk](/ref/snmp.html#snmpwalk) — 从代理返回所有的 SNMP 对象
    -   [snmpwalkoid](/ref/snmp.html#snmpwalkoid) —
        查询关于网络实体的信息树
-   [SNMP](/class/snmp.html) — The SNMP class
    -   [SNMP::close](/class/snmp.html#SNMP::close) — Close SNMP session
    -   [SNMP::\_\_construct](/class/snmp.html#SNMP::__construct) —
        Creates SNMP instance representing session to remote SNMP agent
    -   [SNMP::get](/class/snmp.html#SNMP::get) — Fetch an SNMP object
    -   [SNMP::getErrno](/class/snmp.html#SNMP::getErrno) — Get last
        error code
    -   [SNMP::getError](/class/snmp.html#SNMP::getError) — Get last
        error message
    -   [SNMP::getnext](/class/snmp.html#SNMP::getnext) — Fetch an SNMP
        object which follows the given object id
    -   [SNMP::set](/class/snmp.html#SNMP::set) — Set the value of an
        SNMP object
    -   [SNMP::setSecurity](/class/snmp.html#SNMP::setSecurity) —
        Configures security-related SNMPv3 session parameters
    -   [SNMP::walk](/class/snmp.html#SNMP::walk) — Fetch SNMP object
        subtree
-   [SNMPException](/class/snmpexception.html) — The SNMPException class

简介
----

Represents SNMP session.

类摘要
------

**SNMP**

<span class="ooclass"> class **SNMP** </span> {

/\* 属性 \*/

<span class="modifier">public</span> <span class="type">int</span>
`$max_oids` ;

<span class="modifier">public</span> <span class="type">int</span>
`$valueretrieval` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$quick_print` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$enum_print` ;

<span class="modifier">public</span> <span class="type">int</span>
`$oid_output_format` ;

<span class="modifier">public</span> <span class="type">bool</span>
`$oid_increasing_check` ;

<span class="modifier">public</span> <span class="type">int</span>
`$exceptions_enabled` ;

<span class="modifier">public</span> <span class="type">array</span>
`$info` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> ,
<span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">string</span> `$community`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">close</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">mixed</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$preserve_keys`<span
class="initializer"> = **`false`**</span></span> \] )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getErrno</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getError</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getnext</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object_id`</span>
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">mixed</span> `$object_id`</span> , <span
class="methodparam"><span class="type">mixed</span> `$type`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setSecurity</span> ( <span
class="methodparam"><span class="type">string</span> `$sec_level`</span>
\[, <span class="type">string</span> `$auth_protocol`<span
class="initializer"> = </span> \[, <span class="type">string</span>
`$auth_passphrase`<span class="initializer"> = </span> \[, <span
class="type">string</span> `$priv_protocol`<span class="initializer"> =
</span> \[, <span class="type">string</span> `$priv_passphrase`<span
class="initializer"> = </span> \[, <span class="type">string</span>
`$contextName`<span class="initializer"> = </span> \[, <span
class="type">string</span> `$contextEngineID`<span class="initializer">
= </span> \]\]\]\]\]\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">walk</span> ( <span class="methodparam"><span
class="type">string</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$suffix_as_key`<span
class="initializer"> = **`false`**</span></span> \[, <span
class="methodparam"><span class="type">int</span>
`$max_repetitions`</span> \[, <span class="methodparam"><span
class="type">int</span> `$non_repeaters`</span> \]\]\] )

/\* 常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_NOERROR` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_GENERIC` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_TIMEOUT` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_ERROR_IN_REPLY` <span class="initializer"> = 8</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_OID_NOT_INCREASING` <span class="initializer"> = 16</span>
;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_OID_PARSING_ERROR` <span class="initializer"> = 32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_MULTIPLE_SET_QUERIES` <span class="initializer"> =
64</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::ERRNO_ANY` <span class="initializer"> = 126</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::VERSION_1` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::VERSION_2C` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::VERSION_2c` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SNMP::VERSION_3` <span class="initializer"> = 3</span> ;

}

属性
----

`max_oids`  
Maximum OID per GET/SET/GETBULK request

`valueretrieval`  
Controls the method how the SNMP values will be returned

|                          |                                                                                                                                                                                                                                                                       |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`SNMP_VALUE_LIBRARY`** | The return values will be as returned by the Net-SNMP library.                                                                                                                                                                                                        |
| **`SNMP_VALUE_PLAIN`**   | The return values will be the plain value without the SNMP type hint.                                                                                                                                                                                                 |
| **`SNMP_VALUE_OBJECT`**  | The return values will be objects with the properties "value" and "type", where the latter is one of the SNMP\_OCTET\_STR, SNMP\_COUNTER etc. constants. The way "value" is returned is based on which one of **`SNMP_VALUE_LIBRARY`**, **`SNMP_VALUE_PLAIN`** is set |

`quick_print`  
Value of `quick_print` within the NET-SNMP library

Sets the value of `quick_print` within the NET-SNMP library. When this
is set (1), the SNMP library will return 'quick printed' values. This
means that just the value will be printed. When `quick_print` is not
enabled (default) the UCD SNMP library prints extra information
including the type of the value (i.e. IpAddress or OID). Additionally,
if quick\_print is not enabled, the library prints additional hex values
for all strings of three characters or less.

`enum_print`  
Controls the way enum values are printed

Parameter toggles if walk/get etc. should automatically lookup enum
values in the MIB and return them together with their human readable
string.

`oid_output_format`  
Controls OID output format

|                               |                                                                     |
|-------------------------------|---------------------------------------------------------------------|
| **`SNMP_OID_OUTPUT_FULL`**    | .iso.org.dod.internet.mgmt.mib-2.system.sysUpTime.sysUpTimeInstance |
| **`SNMP_OID_OUTPUT_NUMERIC`** | .1.3.6.1.2.1.1.3.0                                                  |
| **`SNMP_OID_OUTPUT_MODULE`**  | DISMAN-EVENT-MIB::sysUpTimeInstance                                 |
| **`SNMP_OID_OUTPUT_SUFFIX`**  | sysUpTimeInstance                                                   |
| **`SNMP_OID_OUTPUT_UCD`**     | system.sysUpTime.sysUpTimeInstance                                  |
| **`SNMP_OID_OUTPUT_NONE`**    | Undefined                                                           |

`oid_increasing_check`  
Controls disabling check for increasing OID while walking OID tree

Some SNMP agents are known for returning OIDs out of order but can
complete the walk anyway. Other agents return OIDs that are out of order
and can cause <span class="methodname">SNMP::walk</span> to loop
indefinitely until memory limit will be reached. PHP SNMP library by
default performs OID increasing check and stops walking on OID tree when
it detects possible loop with issuing warning about non-increasing OID
faced. Set `oid_increasing_check` to **`false`** to disable this check.

`exceptions_enabled`  
Controls which failures will raise SNMPException instead of warning. Use
bitwise OR'ed **`SNMP::ERRNO_*`** constants. By default all SNMP
exceptions are disabled.

`info`  
Read-only property with remote agent configuration: hostname, port,
default timeout, default retries count

预定义常量
----------

SNMP Error Types
----------------

**`SNMP::ERRNO_NOERROR`**  
No SNMP-specific error occurred.

**`SNMP::ERRNO_GENERIC`**  
A generic SNMP error occurred.

**`SNMP::ERRNO_TIMEOUT`**  
Request to SNMP agent timed out.

**`SNMP::ERRNO_ERROR_IN_REPLY`**  
SNMP agent returned an error in reply.

**`SNMP::ERRNO_OID_NOT_INCREASING`**  
SNMP agent faced OID cycling reporning non-increasing OID while
executing (BULK)WALK command. This indicates bogus remote SNMP agent.

**`SNMP::ERRNO_OID_PARSING_ERROR`**  
Library failed while parsing OID (and/or type for SET command). No
queries has been made.

**`SNMP::ERRNO_MULTIPLE_SET_QUERIES`**  
Library will use multiple queries for SET operation requested. That
means that operation will be performed in a non-transaction manner and
second or subsequent chunks may fail if a type or value failure will be
faced.

**`SNMP::ERRNO_ANY`**  
All SNMP::ERRNO\_\* codes bitwise OR'ed.

SNMP Protocol Versions
----------------------

**`SNMP::VERSION_1`**  

**`SNMP::VERSION_2C`**, **`SNMP::VERSION_2c`**  

**`SNMP::VERSION_3`**  

SNMP::close
===========

Close SNMP session

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SNMP::close</span> ( <span
class="methodparam">void</span> )

Frees previously allocated SNMP session object.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="methodname">SNMP::close</span> example**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  # ...
  # get, walk, etc goes here
  # ...
  $session->close();
?>
```

### 参见

-   <span class="methodname">SNMP::\_\_construct</span>

SNMP::\_\_construct
===================

Creates SNMP instance representing session to remote SNMP agent

### 说明

<span class="modifier">public</span> <span
class="methodname">SNMP::\_\_construct</span> ( <span
class="methodparam"><span class="type">int</span> `$version`</span> ,
<span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">string</span> `$community`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

The function description goes here.

### 参数

`version`  
SNMP protocol version: **`SNMP::VERSION_1`**, **`SNMP::VERSION_2C`**,
**`SNMP::VERSION_3`**.

`hostname`  
The SNMP agent. `hostname` may be suffixed with optional SNMP agent port
after colon. IPv6 addresses must be enclosed in square brackets if used
with port. If FQDN is used for `hostname` it will be resolved by
php-snmp library, not by Net-SNMP engine. Usage of IPv6 addresses when
specifying FQDN may be forced by enclosing FQDN into square brackets.
Here it is some examples:

|                                                      |                      |
|------------------------------------------------------|----------------------|
| IPv4 with default port                               | 127.0.0.1            |
| IPv6 with default port                               | ::1 or \[::1\]       |
| IPv4 with specific port                              | 127.0.0.1:1161       |
| IPv6 with specific port                              | \[::1\]:1161         |
| FQDN with default port                               | host.domain          |
| FQDN with specific port                              | host.domain:1161     |
| FQDN with default port, force usage of IPv6 address  | \[host.domain\]      |
| FQDN with specific port, force usage of IPv6 address | \[host.domain\]:1161 |

`community`  
The purpuse of `community` is SNMP version specific:

|                   |                     |
|-------------------|---------------------|
| SNMP::VERSION\_1  | SNMP community      |
| SNMP::VERSION\_2C | SNMP community      |
| SNMP::VERSION\_3  | SNMPv3 securityName |

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of retries in case timeout occurs.

### 返回值

Returns SNMP object representing remote SNMP agent.

### 错误／异常

<span class="methodname">SNMP::\_\_construct</span> throws an exception
when parameters count or types are wrong or unknown SNMP protocol
version specified.

### 范例

**示例 \#1 Fetching sysLocation**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $sysdescr = $session->get("sysDescr.0");
  echo "$sysdescr\n";
?>
```

以上例程的输出类似于：

    STRING: Test server

### 参见

-   <span class="methodname">SNMP::close</span>

SNMP::get
=========

Fetch an SNMP object

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SNMP::get</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object_id`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$preserve_keys`<span class="initializer"> = **`false`**</span></span>
\] )

Fetch an SNMP object specified in `object_id` using GET query.

### 参数

If `object_id` is a string, then <span
class="methodname">SNMP::get</span> will return SNMP object as string.
If `object_id` is a array, all requested SNMP objects will be returned
as associative array of the SNMP object ids and their values.

`object_id`  
The SNMP object (OID) or objects

`preserve_keys`  
When `object_id` is a array and `preserve_keys` set to **`true`** keys
in results will be taken exactly as in `object_id`, otherwise
`SNMP::oid_output_format` property is used to determinate the form of
keys.

### 返回值

Returns SNMP objects requested as string or array depending on
`object_id` type or **`false`** on error.

### 错误／异常

本方法默认不抛出任何异常。如果要在某些库出错时抛出 SNMPException
异常，用户需要将 SNMP 类参数 `exceptions_enabled`
设定为相应的值。更多细节见
<a href="/class/snmp.html#" class="link"><code class="parameter">SNMP::$exceptions_enabled</code> 的解释</a>。

### 范例

**示例 \#1 Single SNMP object**

Single SNMP object may be requested in two ways: as string resulting
string return value or as single-element array with associative array as
output.

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $sysdescr = $session->get("sysDescr.0");
  echo "$sysdescr\n";
  $sysdescr = $session->get(array("sysDescr.0"));
  print_r($sysdescr);
?>
```

以上例程的输出类似于：

    STRING: Test server
    Array
    (
        [SNMPv2-MIB::sysDescr.0] => STRING: Test server
    )

**示例 \#2 Multiple SNMP objects**

``` php
$session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $results = $session->get(array("sysDescr.0", "sysName.0"));
  print_r($results);
  $session->close();
```

以上例程的输出类似于：

    Array
    (
        [SNMPv2-MIB::sysDescr.0] => STRING: Test server
        [SNMPv2-MIB::sysName.0] => STRING: myhost.nodomain
    )

### 参见

-   <span class="methodname">SNMP::getErrno</span>
-   <span class="methodname">SNMP::getError</span>

SNMP::getErrno
==============

Get last error code

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SNMP::getErrno</span> ( <span
class="methodparam">void</span> )

Returns error code from last SNMP request.

### 返回值

Returns one of SNMP error code values described in constants chapter.

### 范例

**示例 \#1 <span class="methodname">SNMP::getErrno</span> example**

``` php
<?php
$session = new SNMP(SNMP::VERSION_2c, '127.0.0.1', 'boguscommunity');
var_dump(@$session->get('.1.3.6.1.2.1.1.1.0'));
var_dump($session->getErrno() == SNMP::ERRNO_TIMEOUT);
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="methodname">SNMP::getError</span>

SNMP::getError
==============

Get last error message

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SNMP::getError</span> ( <span
class="methodparam">void</span> )

Returns string with error from last SNMP request.

### 返回值

String describing error from last SNMP request.

### 范例

**示例 \#1 <span class="methodname">SNMP::getError</span> example**

``` php
<?php
$session = new SNMP(SNMP::VERSION_2c, '127.0.0.1', 'boguscommunity');
var_dump(@$session->get('.1.3.6.1.2.1.1.1.0'));
var_dump($session->getError());
?>
```

以上例程会输出：

    bool(false)
    string(26) "No response from 127.0.0.1"

### 参见

-   <span class="methodname">SNMP::getErrno</span>

SNMP::getnext
=============

Fetch an SNMP object which follows the given object id

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">SNMP::getnext</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object_id`</span>
)

Fetch an SNMP object that follows specified `object_id`.

### 参数

If `object_id` is a string, then <span
class="methodname">SNMP::getnext</span> will return SNMP object as
string. If `object_id` is a array, all requested SNMP objects will be
returned as associative array of the SNMP object ids and their values.

`object_id`  
The SNMP object (OID) or objects

### 返回值

Returns SNMP objects requested as string or array depending on
`object_id` type or **`false`** on error.

### 错误／异常

本方法默认不抛出任何异常。如果要在某些库出错时抛出 SNMPException
异常，用户需要将 SNMP 类参数 `exceptions_enabled`
设定为相应的值。更多细节见
<a href="/class/snmp.html#" class="link"><code class="parameter">SNMP::$exceptions_enabled</code> 的解释</a>。

### 范例

**示例 \#1 Single SNMP object**

Single SNMP object may be requested in two ways: as string resulting
string return value or as single-element array with associative array as
output.

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $nsysdescr = $session->getnext("sysDescr.0");
  echo "$nsysdescr\n";
  $nsysdescr = $session->getnext(array("sysDescr.0"));
  print_r($nsysdescr);
?>
```

以上例程的输出类似于：

    OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
    Array
    (
        [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
    )

**示例 \#2 Miltiple SNMP objects**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $results = $session->getnext(array("sysDescr.0", "sysName.0"));
  print_r($results);
  $session->close();
?>
```

以上例程的输出类似于：

    Array
    (
        [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
        [SNMPv2-MIB::sysLocation.0] => STRING: Nowhere
    )

### 参见

-   <span class="methodname">SNMP::getErrno</span>
-   <span class="methodname">SNMP::getError</span>

SNMP::set
=========

Set the value of an SNMP object

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SNMP::set</span> ( <span
class="methodparam"><span class="type">mixed</span> `$object_id`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$type`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

Requests remote SNMP agent setting the value of one or more SNMP objects
specified by the `object_id`.

### 参数

`object_id`  
The SNMP object id

When count of OIDs in object\_id array is greater than max\_oids object
property set method will have to use multiple queries to perform
requested value updates. In this case type and value checks are made
per-chunk so second or subsequent requests may fail due to wrong type or
value for OID requested. To mark this a warning is raised when count of
OIDs in object\_id array is greater than max\_oids.

`type`  
MIB 定义了各个对象 id 的类型。必须是下面列出的单个字符之一。

|     |                |
|-----|----------------|
| =   | MIB类型        |
| i   | INTEGER        |
| u   | INTEGER        |
| s   | STRING         |
| x   | HEX STRING     |
| d   | DECIMAL STRING |
| n   | NULLOBJ        |
| o   | OBJID          |
| t   | TIMETICKS      |
| a   | IPADDRESS      |
| b   | BITS           |

如果在编译 SNMP 库时定义了
**`OPAQUE_SPECIAL_TYPES`**，那么下列值是合法的：

|     |                |
|-----|----------------|
| U   | unsigned int64 |
| I   | signed int64   |
| F   | float          |
| D   | double         |

这些值大都会使用与 ASN.1 相符的类型。's'，'x'，'d' 以及 'b'
都是指定一个八字节字符串值的方式。并且 'u' 无符号类型也可用于处理
Gauge32 值。

如果 MIB 文件是用 "snmp\_read\_mib" 或者通过在 libsnmp config
中指定而加载入 MIB 树时， '=' 可以被用作为所有对象的 `type` 参数，因为
type 可以被自动从 MIB 中读取。

注意有两种方式可以设定 BITS 类型的变量，例如 "SYNTAX BITS {telnet(0),
ftp(1), http(2), icmp(3), snmp(4), ssh(5), https(6)}":

-   <span class="simpara"> 使用 "b"
    类型以及一个位数的列表。不推荐使用此方法，因为 GET 查询对同一个 OID
    将会返回例如 0xF8。 </span>
-   <span class="simpara"> 使用 "x"
    类型以及一个十六进制数但是不需要通常的 "0x" 前缀。 </span>

更多细节见范例部分。

`value`  
The new value.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

本方法默认不抛出任何异常。如果要在某些库出错时抛出 SNMPException
异常，用户需要将 SNMP 类参数 `exceptions_enabled`
设定为相应的值。更多细节见
<a href="/class/snmp.html#" class="link"><code class="parameter">SNMP::$exceptions_enabled</code> 的解释</a>。

### 范例

**示例 \#1 Set single SNMP object id**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set('SNMPv2-MIB::sysContact.0', 's', "Nobody");
?>
```

**示例 \#2 Set multiple values using single <span
class="methodname">SNMP::set</span> call**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set(array('SNMPv2-MIB::sysContact.0', 'SNMPv2-MIB::sysLocation.0'), array('s', 's'), array("Nobody", "Nowhere"));
// or
  $session->set(array('SNMPv2-MIB::sysContact.0', 'SNMPv2-MIB::sysLocation.0'), 's', array("Nobody", "Nowhere"));
?>
```

**示例 \#3 Using <span class="methodname">SNMP::set</span> for setting
BITS SNMP object id**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set('FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// or
  $session->set('FOO-MIB::bar.42', 'x', 'F0');
?>
```

### 参见

-   <span class="methodname">SNMP::get</span>

SNMP::setSecurity
=================

Configures security-related SNMPv3 session parameters

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SNMP::setSecurity</span> ( <span
class="methodparam"><span class="type">string</span> `$sec_level`</span>
\[, <span class="type">string</span> `$auth_protocol`<span
class="initializer"> = </span> \[, <span class="type">string</span>
`$auth_passphrase`<span class="initializer"> = </span> \[, <span
class="type">string</span> `$priv_protocol`<span class="initializer"> =
</span> \[, <span class="type">string</span> `$priv_passphrase`<span
class="initializer"> = </span> \[, <span class="type">string</span>
`$contextName`<span class="initializer"> = </span> \[, <span
class="type">string</span> `$contextEngineID`<span class="initializer">
= </span> \]\]\]\]\]\] )

setSecurity configures security-related session parameters used in SNMP
protocol version 3

### 参数

`sec_level`  
the security level (noAuthNoPriv\|authNoPriv\|authPriv)

`auth_protocol`  
the authentication protocol (MD5 or SHA)

`auth_passphrase`  
the authentication pass phrase

`priv_protocol`  
the privacy protocol (DES or AES)

`priv_passphrase`  
the privacy pass phrase

`contextName`  
the context name

`contextEngineID`  
the context EngineID

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="methodname">SNMP::setSecurity</span> example**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_3, $hostname, $rwuser, $timeout, $retries);
  $session->setSecurity('authPriv', 'MD5', $auth_pass, 'AES', $priv_pass, '', 'aeeeff');
?>
```

### 参见

-   <span class="methodname">SNMP::\_\_construct</span>

SNMP::walk
==========

Fetch SNMP object subtree

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SNMP::walk</span> ( <span
class="methodparam"><span class="type">string</span> `$object_id`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$suffix_as_key`<span class="initializer"> = **`false`**</span></span>
\[, <span class="methodparam"><span class="type">int</span>
`$max_repetitions`</span> \[, <span class="methodparam"><span
class="type">int</span> `$non_repeaters`</span> \]\]\] )

<span class="methodname">SNMP::walk</span> is used to read SNMP subtree
rooted at specified `object_id`.

### 参数

`object_id`  
Root of subtree to be fetched

`suffix_as_key`  
By default full OID notation is used for keys in output array. If set to
**`true`** subtree prefix will be removed from keys leaving only suffix
of object\_id.

`non_repeaters`  
This specifies the number of supplied variables that should not be
iterated over. The default is to use this value from SNMP object.

`max_repetitions`  
This specifies the maximum number of iterations over the repeating
variables. The default is to use this value from SNMP object.

### 返回值

Returns an associative array of the SNMP object ids and their values on
success or **`false`** on error. When a SNMP error occures <span
class="methodname">SNMP::getErrno</span> and <span
class="methodname">SNMP::getError</span> can be used for retrieving
error number (specific to SNMP extension, see class constants) and error
message respectively.

### 错误／异常

本方法默认不抛出任何异常。如果要在某些库出错时抛出 SNMPException
异常，用户需要将 SNMP 类参数 `exceptions_enabled`
设定为相应的值。更多细节见
<a href="/class/snmp.html#" class="link"><code class="parameter">SNMP::$exceptions_enabled</code> 的解释</a>。

### 范例

**示例 \#1 <span class="methodname">SNMP::walk</span> example**

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $fulltree = $session->walk(".");
  print_r($fulltree);
  $session->close();
?>
```

以上例程的输出类似于：

    Array
    (
        [SNMPv2-MIB::sysDescr.0] => STRING: Test server
        [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
        [DISMAN-EVENT-MIB::sysUpTimeInstance] => Timeticks: (1150681750) 133 days, 4:20:17.50
        [SNMPv2-MIB::sysContact.0] => STRING: Nobody
        [SNMPv2-MIB::sysName.0] => STRING: server.localdomain
        ...
    )

**示例 \#2 `suffix_as_key` example**

`suffix_as_key` may be used when merging multiple SNMP subtrees into
one. This example maps interface names to their type.

``` php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $session->valueretrieval = SNMP_VALUE_PLAIN;
  $ifDescr = $session->walk(".1.3.6.1.2.1.2.2.1.2", TRUE);
  $session->valueretrieval = SNMP_VALUE_LIBRARY;
  $ifType = $session->walk(".1.3.6.1.2.1.2.2.1.3", TRUE);
  print_r($ifDescr);
  print_r($ifType);
  $result = array();
  foreach($ifDescr as $i => $n) {
    $result[$n] = $ifType[$i];
  }
  print_r($result);
?>
```

以上例程的输出类似于：

    Array
    (
        [1] => igb0
        [2] => igb1
        [3] => ipfw0
        [4] => lo0
        [5] => lagg0
    )
    Array
    (
        [1] => INTEGER: ieee8023adLag(161)
        [2] => INTEGER: ieee8023adLag(161)
        [3] => INTEGER: ethernetCsmacd(6)
        [4] => INTEGER: softwareLoopback(24)
        [5] => INTEGER: ethernetCsmacd(6)
    )
    Array
    (
        [igb0] => INTEGER: ieee8023adLag(161)
        [igb1] => INTEGER: ieee8023adLag(161)
        [ipfw0] => INTEGER: ethernetCsmacd(6)
        [lo0] => INTEGER: softwareLoopback(24)
        [lagg0] => INTEGER: ethernetCsmacd(6)
    )

### 参见

-   <span class="methodname">SNMP::getErrno</span>
-   <span class="methodname">SNMP::getError</span>

简介
----

Represents an error raised by SNMP. You should not throw a <span
class="classname">SNMPException</span> from your own code. See
<a href="/language/exceptions.html" class="link">Exceptions</a> for more
information about Exceptions in PHP.

类摘要
------

**SNMPException**

<span class="ooclass"> class **SNMPException** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**RuntimeException** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$code` ;

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

`code`  
*SNMP*library error code. Use <span
class="function">Exception::getCode</span> to access it.
