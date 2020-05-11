snmp\_get\_quick\_print
=======================

返回 UCD 库中 quick\_print 设置的当前值

### 说明

<span class="type">bool</span> <span
class="methodname">snmp\_get\_quick\_print</span> ( <span
class="methodparam">void</span> )

返回保存在 UCD 库中 quick\_print 的当前值。默认情况下 quick\_print 为
off。

**示例 \#1 <span class="function">snmp\_get\_quick\_print</span> 示例**

``` php
<?php
  $quickprint = snmp_get_quick_print();
?>
```

如果 quick\_print 为 off，上边的函数调用将返回 **`FALSE`**，而如果
quick\_print 为 on，则返回 **`TRUE`**。

<span class="function">snmp\_get\_quick\_print</span> 仅在使用了 UCD
SNMP 库时才可用。当使用 Windows SNMP 库时，此函数不可用。

参见 <span class="function">snmp\_set\_quick\_print</span> 查看
quick\_print 的详细说明。

snmp\_get\_valueretrieval
=========================

Return the method how the SNMP values will be returned

### 说明

<span class="type">int</span> <span
class="methodname">snmp\_get\_valueretrieval</span> ( <span
class="methodparam">void</span> )

### 返回值

OR-ed combitantion of constants ( **`SNMP_VALUE_LIBRARY`** or
**`SNMP_VALUE_PLAIN`** ) with possible SNMP\_VALUE\_OBJECT set.

### 范例

**示例 \#1 Using snmp\_get\_valueretrieval**

``` php
<?php
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 if (snmp_get_valueretrieval() & SNMP_VALUE_OBJECT) {
   echo $ret->value;
 } else {
   echo $ret;
 }
?>
```

### 参见

-   <span class="function">snmp\_set\_valueretrieval</span>
-   <a href="/snmp/constants.html" class="xref">预定义常量</a>

snmp\_read\_mib
===============

Reads and parses a MIB file into the active MIB tree

### 说明

<span class="type">bool</span> <span
class="methodname">snmp\_read\_mib</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

This function is used to load additional, e.g. vendor specific, MIBs so
that human readable OIDs like VENDOR-MIB::foo.1 instead of error prone
numeric OIDs can be used.

The order in which the MIBs are loaded does matter as the underlying
Net-SNMP libary will print warnings if referenced objects cannot be
resolved.

### 参数

`filename`  
The filename of the MIB.

### 范例

**示例 \#1 Using <span class="function">snmp\_read\_mib</span>**

``` php
<?php
 print_r( snmprealwalk('localhost', 'public', '.1.3.6.1.2.1.2.3.4.5') );
 
 snmp_read_mib('./FOO-BAR-MIB.txt');
 print_r( snmprealwalk('localhost', 'public', 'FOO-BAR-MIB::someTable' );
?>
```

The above example is made up but the results would look like:

         
    Array
    (
        [iso.3.6.1.2.1.2.3.4.5.0] => Gauge32: 6
    )
    Array
    (
        [FOO-BAR-MIB::someTable.0] => Gauge32: 6
    )

snmp\_set\_enum\_print
======================

Return all values that are enums with their enum value instead of the
raw integer

### 说明

<span class="type">bool</span> <span
class="methodname">snmp\_set\_enum\_print</span> ( <span
class="methodparam"><span class="type">int</span> `$enum_print`</span> )

This function toggles if snmpwalk/snmpget etc. should automatically
lookup enum values in the MIB and return them together with their human
readable string.

### 参数

`enum_print`  
As the value is interpreted as boolean by the Net-SNMP library, it can
only be "0" or "1".

### 范例

**示例 \#1 Using <span class="function">snmp\_set\_enum\_print</span>**

``` php
<?php
 snmp_set_enum_print(0);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
 snmp_set_enum_print(1);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
?>
```

The above would return

          
     INTEGER: up(1)
     INTEGER: 1

### 注释

> **Note**:
>
> <span class="function">snmp\_set\_enum\_print</span> is only available
> when using the UCD SNMP library. This function is not available when
> using the Windows SNMP library.

snmp\_set\_oid\_numeric\_print
==============================

Set the OID output format

### 说明

<span class="type">void</span> <span
class="methodname">snmp\_set\_oid\_numeric\_print</span> ( <span
class="methodparam"><span class="type">int</span> `$oid_format`</span> )

此函数是该函数的别名： <span
class="function">snmp\_set\_oid\_output\_format</span>.

### 更新日志

| 版本  | 说明                                                                                           |
|-------|------------------------------------------------------------------------------------------------|
| 5.2.0 | This function is now an alias of <span class="function">snmp\_set\_oid\_output\_format</span>. |

### 参见

-   <span class="function">snmp\_set\_oid\_output\_format</span>

snmp\_set\_oid\_output\_format
==============================

Set the OID output format

### 说明

<span class="type">bool</span> <span
class="methodname">snmp\_set\_oid\_output\_format</span> ( <span
class="methodparam"><span class="type">int</span> `$oid_format`<span
class="initializer"> = SNMP\_OID\_OUTPUT\_MODULE</span></span> )

<span class="function">snmp\_set\_oid\_output\_format</span> sets the
output format to be full or numeric.

### 参数

`oid_format`  
|                               |                                                                     |
|-------------------------------|---------------------------------------------------------------------|
| **`SNMP_OID_OUTPUT_FULL`**    | .iso.org.dod.internet.mgmt.mib-2.system.sysUpTime.sysUpTimeInstance |
| **`SNMP_OID_OUTPUT_NUMERIC`** | .1.3.6.1.2.1.1.3.0                                                  |

Begining from PHP 5.4.0 four additional constants available:

|                              |                                     |
|------------------------------|-------------------------------------|
| **`SNMP_OID_OUTPUT_MODULE`** | DISMAN-EVENT-MIB::sysUpTimeInstance |
| **`SNMP_OID_OUTPUT_SUFFIX`** | sysUpTimeInstance                   |
| **`SNMP_OID_OUTPUT_UCD`**    | system.sysUpTime.sysUpTimeInstance  |
| **`SNMP_OID_OUTPUT_NONE`**   | Undefined                           |

### 返回值

没有返回值。

### 注释

> **Note**:
>
> <span class="function">snmp\_set\_oid\_output\_format</span> is only
> available when using the UCD SNMP library. This function is not
> available when using the Windows SNMP library.

### 范例

**示例 \#1 Using <span class="function">snmprealwalk</span>**

``` php
<?php

 snmp_read_mib("/usr/share/mibs/netsnmp/NET-SNMP-TC");

 // default or SNMP_OID_OUTPUT_MODULE in PHP >= 5.3.6
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );

 snmp_set_oid_output_format(SNMP_OID_OUTPUT_NUMERIC);
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );

 snmp_set_oid_output_format(SNMP_OID_OUTPUT_FULL);
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );
?>
```

The above would output:

     Array
     (
        [RFC1213-MIB::sysObjectID.0] => OID: NET-SNMP-TC::linux
     )
     Array
     (
        [.1.3.6.1.2.1.1.2.0] => OID: .1.3.6.1.4.1.8072.3.2.10
     )
     Array
     (
        [.iso.org.dod.internet.mgmt.mib-2.system.sysObjectID.0] => OID: .iso.org.dod.internet.private.enterprises.netSnmp.netSnmpEnumerations.netSnmpAgentOIDs.linux
     )

snmp\_set\_quick\_print
=======================

设置 UCD SNMP 库中 quick\_print 的值

### 说明

<span class="type">void</span> <span
class="methodname">snmp\_set\_quick\_print</span> ( <span
class="methodparam"><span class="type">bool</span> `$quick_print`</span>
)

设置 UCD SNMP 库中 quick\_print 的值。当此值被设置（1），SNMP
库将返回‘快速打印’值。这意味着将只打印值。当 quick\_print
被禁用时（此为默认情况），UCD SNMP 库将打印出额外信息，包括值的类型（如
IpAddress 或 OID）。此外，如果 quick\_print 是禁用的，UCD SNMP
库将为所有字符串额外打印出三个或更少字符的十六进制值。

当需要使用返回的信息而不是显示它时，经常会用到设置 quick\_print。

``` php
<?php
snmp_set_quick_print(0);
$a = snmpget("127.0.0.1", "public", ".1.3.6.1.2.1.2.2.1.9.1");
echo "$a< br />\n";
snmp_set_quick_print(1);
$a = snmpget("127.0.0.1", "public", ".1.3.6.1.2.1.2.2.1.9.1");
echo "$a<br />\n";
?>
```

第一个打印出来的值可能时：'Timeticks: (0) 0:00:00.00'，然而当设置了
quick\_print 之后，只是打印 '0:00:00.00'。

默认情况下 UCD SNMP 库返回冗余的值，而 quick\_print 则用来只返回值。

现时，字符串依然返回额外的引号，这将会在后续发行版中更正。

<span class="function">snmp\_set\_quick\_print</span> 仅在使用了 UCD
SNMP 库时才可用。当使用 Windows SNMP 库时，此函数不可用。

snmp\_set\_valueretrieval
=========================

Specify the method how the SNMP values will be returned

### 说明

<span class="type">bool</span> <span
class="methodname">snmp\_set\_valueretrieval</span> ( <span
class="methodparam"> <span class="type">int</span> `$method` <span
class="initializer"> = SNMP\_VALUE\_LIBRARY</span> </span> )

### 参数

`method`  
|                      |                                                                                                                                                                                                                                                                                  |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMP\_VALUE\_LIBRARY | The return values will be as returned by the Net-SNMP library.                                                                                                                                                                                                                   |
| SNMP\_VALUE\_PLAIN   | The return values will be the plain value without the SNMP type hint.                                                                                                                                                                                                            |
| SNMP\_VALUE\_OBJECT  | The return values will be objects with the properties "value" and "type", where the latter is one of the SNMP\_OCTET\_STR, SNMP\_COUNTER etc. constants. The way "value" is returned is based on which one of constants **`SNMP_VALUE_LIBRARY`**, **`SNMP_VALUE_PLAIN`** is set. |

### 范例

**示例 \#1 Using <span
class="function">snmp\_set\_valueretrieval</span>**

``` php
<?php
 snmp_set_valueretrieval(SNMP_VALUE_LIBRARY);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // $ret = "STRING: lo"

 snmp_set_valueretrieval(SNMP_VALUE_PLAIN);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // $ret = "lo";

 snmp_set_valueretrieval(SNMP_VALUE_OBJECT);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, see constants
 //   [value] => lo
 // )

 // PHP 5.4+ examples
 snmp_set_valueretrieval(SNMP_VALUE_OBJECT | SNMP_VALUE_PLAIN);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, see constants
 //   [value] => lo
 // )

 snmp_set_valueretrieval(SNMP_VALUE_OBJECT | SNMP_VALUE_LIBRARY);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, see constants
 //   [value] => STRING: lo
 // )

?>
```

### 更新日志

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>版本</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>5.4.0</td>
<td><p>Constants <strong><code>SNMP_VALUE_PLAIN</code></strong> or <strong><code>SNMP_VALUE_LIBRARY</code></strong> may be combined with <strong><code>SNMP_VALUE_OBJECT</code></strong> resulting different way of representing contents of <code class="parameter">value</code> array element in return value of GET-function. If no <strong><code>SNMP_VALUE_{PLAIN,LIBRARY}</code></strong> constant is accompanying <strong><code>SNMP_VALUE_OBJECT</code></strong>, <strong><code>SNMP_VALUE_LIBRARY</code></strong> is used.</p>
<p>Prior to 5.4.0 <strong><code>SNMP_VALUE_OBJECT</code></strong> effecively meant <strong><code>SNMP_VALUE_OBJECT</code></strong>|<strong><code>SNMP_VALUE_PLAIN</code></strong>.</p></td>
</tr>
</tbody>
</table>

### 参见

-   <span class="function">snmp\_get\_valueretrieval</span>
-   <a href="/snmp/constants.html" class="xref">预定义常量</a>

snmp2\_get
==========

Fetch an SNMP object

### 说明

<span class="type">string</span> <span
class="methodname">snmp2\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
1000000</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`<span class="initializer"> =
5</span></span> \]\] )

The <span class="function">snmp2\_get</span> function is used to read
the value of an SNMP object specified by the `object_id`.

### 参数

`host`  
The SNMP agent.

`community`  
The read community.

`object_id`  
The SNMP object.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns SNMP object value on success or **`FALSE`** on error.

### 范例

**示例 \#1 Using <span class="function">snmp2\_get</span>**

``` php
<?php
$syscontact = snmp2_get("127.0.0.1", "public", "system.SysContact.0");
?>
```

### 参见

-   <span class="function">snmp2\_set</span>

snmp2\_getnext
==============

Fetch the SNMP object which follows the given object id

### 说明

<span class="type">string</span> <span
class="methodname">snmp2\_getnext</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">string</span>
`$community`</span> , <span class="methodparam"><span
class="type">string</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

The <span class="function">snmp2\_get\_next</span> function is used to
read the value of the SNMP object that follows the specified
`object_id`.

### 参数

`host`  
The hostname of the SNMP agent (server).

`community`  
The read community.

`object_id`  
The SNMP object id which precedes the wanted one.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns SNMP object value on success or **`FALSE`** on error. In case of
an error, an E\_WARNING message is shown.

### 范例

**示例 \#1 Using <span class="function">snmp2\_get\_next</span>**

``` php
<?php
$nameOfSecondInterface = snmp2_get_next('localhost', 'public', 'IF-MIB::ifName.1';
?>
```

### 参见

-   <span class="function">snmp2\_get</span>
-   <span class="function">snmp2\_walk</span>

snmp2\_real\_walk
=================

Return all objects including their respective object ID within the
specified one

### 说明

<span class="type">array</span> <span
class="methodname">snmp2\_real\_walk</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">string</span>
`$community`</span> , <span class="methodparam"><span
class="type">string</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

The <span class="function">snmp2\_real\_walk</span> function is used to
traverse over a number of SNMP objects starting from `object_id` and
return not only their values but also their object ids.

### 参数

`host`  
The hostname of the SNMP agent (server).

`community`  
The read community.

`object_id`  
The SNMP object id which precedes the wanted one.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns an associative array of the SNMP object ids and their values on
success or **`FALSE`** on error. In case of an error, an E\_WARNING
message is shown.

### 范例

**示例 \#1 Using <span class="function">snmp2\_real\_walk</span>**

``` php
<?php
 print_r(snmp2_real_walk("localhost", "public", "IF-MIB::ifName"));
?>
```

The above will output something like:

        Array
          (
          [IF-MIB::ifName.1] => STRING: lo
          [IF-MIB::ifName.2] => STRING: eth0
          [IF-MIB::ifName.3] => STRING: eth2
          [IF-MIB::ifName.4] => STRING: sit0
          [IF-MIB::ifName.5] => STRING: sixxs
        )

### 参见

-   <span class="function">snmp2\_walk</span>

snmp2\_set
==========

Set the value of an SNMP object

### 说明

<span class="type">bool</span> <span
class="methodname">snmp2\_set</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> , <span class="methodparam"><span
class="type">string</span> `$type`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> \[,
<span class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

<span class="function">snmp2\_set</span> is used to set the value of an
SNMP object specified by the `object_id`.

### 参数

`host`  
The hostname of the SNMP agent (server).

`community`  
The write community.

`object_id`  
The SNMP object id.

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

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

If the SNMP host rejects the data type, an E\_WARNING message like
"Warning: Error in packet. Reason: (badValue) The value given has the
wrong type or length." is shown. If an unknown or invalid OID is
specified the warning probably reads "Could not add variable".

### 范例

**示例 \#1 Using <span class="function">snmp2\_set</span>**

``` php
<?php
  snmp2_set("localhost", "public", "IF-MIB::ifAlias.3", "s", "foo");
?>
```

**示例 \#2 Using <span class="function">snmp2\_set</span> for setting
BITS SNMP object id**

``` php
<?php
  snmp2_set("localhost", "public", 'FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// or
  snmp2_set("localhost", "public", 'FOO-MIB::bar.42', 'x', 'F0');
?>
```

### 参见

-   <span class="function">snmp2\_get</span>

snmp2\_walk
===========

Fetch all the SNMP objects from an agent

### 说明

<span class="type">array</span> <span
class="methodname">snmp2\_walk</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
1000000</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`<span class="initializer"> =
5</span></span> \]\] )

<span class="function">snmp2\_walk</span> function is used to read all
the values from an SNMP agent specified by the `hostname`.

### 参数

`host`  
The SNMP agent (server).

`community`  
The read community.

`object_id`  
If **`NULL`**, `object_id` is taken as the root of the SNMP objects tree
and all objects under that tree are returned as an array.

If `object_id` is specified, all the SNMP objects below that `object_id`
are returned.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns an array of SNMP object values starting from the `object_id` as
root or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">snmp2\_walk</span> Example**

``` php
<?php
$a = snmp2_walk("127.0.0.1", "public", "");

foreach ($a as $val) {
    echo "$val\n";
}

?>
```

Above function call would return all the SNMP objects from the SNMP
agent running on localhost. One can step through the values with a loop

### 参见

-   <span class="function">snmp2\_real\_walk</span>

snmp3\_get
==========

Fetch an SNMP object

### 说明

<span class="type">string</span> <span
class="methodname">snmp3\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$sec_name`</span>
, <span class="methodparam"><span class="type">string</span>
`$sec_level`</span> , <span class="methodparam"><span
class="type">string</span> `$auth_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$auth_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$priv_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$priv_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

The <span class="function">snmp3\_get</span> function is used to read
the value of an SNMP object specified by the `object_id`.

### 参数

`host`  
The hostname of the SNMP agent (server).

`sec_name`  
the security name, usually some kind of username

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

`object_id`  
The SNMP object id.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns SNMP object value on success or **`FALSE`** on error.

### 范例

**示例 \#1 Using <span class="function">snmp3\_get</span>**

``` php
<?php
$nameOfSecondInterface = snmp3_get('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.2');
?>
```

### 参见

-   <span class="function">snmp3\_set</span>

snmp3\_getnext
==============

Fetch the SNMP object which follows the given object id

### 说明

<span class="type">string</span> <span
class="methodname">snmp3\_getnext</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> ,
<span class="methodparam"><span class="type">string</span>
`$sec_name`</span> , <span class="methodparam"><span
class="type">string</span> `$sec_level`</span> , <span
class="methodparam"><span class="type">string</span>
`$auth_protocol`</span> , <span class="methodparam"><span
class="type">string</span> `$auth_passphrase`</span> , <span
class="methodparam"><span class="type">string</span>
`$priv_protocol`</span> , <span class="methodparam"><span
class="type">string</span> `$priv_passphrase`</span> , <span
class="methodparam"><span class="type">string</span> `$object_id`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`<span class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

The <span class="function">snmp3\_getnext</span> function is used to
read the value of the SNMP object that follows the specified
`object_id`.

### 参数

`host`  
The hostname of the SNMP agent (server).

`sec_name`  
the security name, usually some kind of username

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

`object_id`  
The SNMP object id.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns SNMP object value on success or **`FALSE`** on error. In case of
an error, an E\_WARNING message is shown.

### 范例

**示例 \#1 Using <span class="function">snmp3\_getnext</span>**

``` php
<?php
$nameOfSecondInterface = snmp3_getnext('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.1');
?>
```

### 参见

-   <span class="function">snmp3\_get</span>
-   <span class="function">snmp3\_walk</span>

snmp3\_real\_walk
=================

Return all objects including their respective object ID within the
specified one

### 说明

<span class="type">array</span> <span
class="methodname">snmp3\_real\_walk</span> ( <span class="methodparam">
<span class="type">string</span> `$host` </span> , <span
class="methodparam"> <span class="type">string</span> `$sec_name`
</span> , <span class="methodparam"> <span class="type">string</span>
`$sec_level` </span> , <span class="methodparam"> <span
class="type">string</span> `$auth_protocol` </span> , <span
class="methodparam"> <span class="type">string</span> `$auth_passphrase`
</span> , <span class="methodparam"> <span class="type">string</span>
`$priv_protocol` </span> , <span class="methodparam"> <span
class="type">string</span> `$priv_passphrase` </span> , <span
class="methodparam"> <span class="type">string</span> `$object_id`
</span> \[, <span class="methodparam"> <span class="type">int</span>
`$timeout` <span class="initializer"> = 1000000</span> </span> \[, <span
class="methodparam"> <span class="type">int</span> `$retries` <span
class="initializer"> = 5</span> </span> \]\] )

The <span class="function">snmp3\_real\_walk</span> function is used to
traverse over a number of SNMP objects starting from `object_id` and
return not only their values but also their object ids.

### 参数

`host`  
The hostname of the SNMP agent (server).

`sec_name`  
the security name, usually some kind of username

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

`object_id`  
The SNMP object id.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns an associative array of the SNMP object ids and their values on
success or **`FALSE`** on error. In case of an error, an E\_WARNING
message is shown.

### 范例

**示例 \#1 Using <span class="function">snmp3\_real\_walk</span>**

``` php
<?php
 var_export(snmp3_real_walk('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName'));
?>
```

The above will output something like:

    array (
      'IF-MIB::ifName.1' => 'STRING: lo',
      'IF-MIB::ifName.2' => 'STRING: eth0',
      'IF-MIB::ifName.3' => 'STRING: eth2',
      'IF-MIB::ifName.4' => 'STRING: sit0',
      'IF-MIB::ifName.5' => 'STRING: sixxs',
    )

### 参见

-   <span class="function">snmpwalk</span>

snmp3\_set
==========

Set the value of an SNMP object

### 说明

<span class="type">bool</span> <span
class="methodname">snmp3\_set</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$sec_name`</span>
, <span class="methodparam"><span class="type">string</span>
`$sec_level`</span> , <span class="methodparam"><span
class="type">string</span> `$auth_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$auth_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$priv_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$priv_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$object_id`</span> , <span
class="methodparam"><span class="type">string</span> `$type`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
1000000</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`<span class="initializer"> =
5</span></span> \]\] )

<span class="function">snmp3\_set</span> is used to set the value of an
SNMP object specified by the `object_id`.

Even if the security level does not use an auth or priv
protocol/password valid values have to be specified.

### 参数

`host`  
The hostname of the SNMP agent (server).

`sec_name`  
the security name, usually some kind of username

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

`object_id`  
The SNMP object id.

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
The new value

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

If the SNMP host rejects the data type, an E\_WARNING message like
"Warning: Error in packet. Reason: (badValue) The value given has the
wrong type or length." is shown. If an unknown or invalid OID is
specified the warning probably reads "Could not add variable".

### 范例

**示例 \#1 Using <span class="function">snmp3\_set</span>**

``` php
<?php
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifAlias.3', 's', "foo");
?>
```

**示例 \#2 Using <span class="function">snmp3\_set</span> for setting
BITS SNMP object id**

``` php
<?php
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// or
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'FOO-MIB::bar.42', 'x', 'F0');
?>
```

snmp3\_walk
===========

Fetch all the SNMP objects from an agent

### 说明

<span class="type">array</span> <span
class="methodname">snmp3\_walk</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$sec_name`</span>
, <span class="methodparam"><span class="type">string</span>
`$sec_level`</span> , <span class="methodparam"><span
class="type">string</span> `$auth_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$auth_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$priv_protocol`</span> , <span
class="methodparam"><span class="type">string</span>
`$priv_passphrase`</span> , <span class="methodparam"><span
class="type">string</span> `$object_id`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 1000000</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`<span
class="initializer"> = 5</span></span> \]\] )

<span class="function">snmp3\_walk</span> function is used to read all
the values from an SNMP agent specified by the `hostname`.

Even if the security level does not use an auth or priv
protocol/password valid values have to be specified.

### 参数

`host`  
The hostname of the SNMP agent (server).

`sec_name`  
the security name, usually some kind of username

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

`object_id`  
If **`NULL`**, `object_id` is taken as the root of the SNMP objects tree
and all objects under that tree are returned as an array.

If `object_id` is specified, all the SNMP objects below that `object_id`
are returned.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns an array of SNMP object values starting from the `object_id` as
root or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">snmp3\_walk</span> Example**

``` php
<?php
$ret = snmp3_walk('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName');
var_export($ret);
?>
```

Above function call would return all the SNMP objects from the SNMP
agent running on localhost:

          
    array (
      0 => 'STRING: lo',
      1 => 'STRING: eth0',
      2 => 'STRING: eth2',
      3 => 'STRING: sit0',
      4 => 'STRING: sixxs',
    )

### 参见

-   <span class="function">snmp3\_real\_walk</span>

snmpget
=======

获取一个 SNMP 对象

### 说明

<span class="type">string</span> <span class="methodname">snmpget</span>
( <span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">string</span> `$community`</span> , <span
class="methodparam"><span class="type">string</span> `$object_id`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`</span> \]\] )

成功则返回 SNMP 的对象值，失败则返回 **`FALSE`**。

函数 <span class="function">snmpget</span> 用于读取由 `object_id` 指定的
SNMP 对象值。`hostname` 指定 SNMP 代理，而 `community`
参数指定具有读权限的域的名字。

``` php
<?php
$syscontact = snmpget("127.0.0.1", "public", "system.SysContact.0");
?>
```

snmpgetnext
===========

Fetch the SNMP object which follows the given object id

### 说明

<span class="type">string</span> <span
class="methodname">snmpgetnext</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
1000000</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`<span class="initializer"> =
5</span></span> \]\] )

The <span class="function">snmpgetnext</span> function is used to read
the value of the SNMP object that follows the specified `object_id`.

### 参数

`host`  
The hostname of the SNMP agent (server).

`community`  
The read community.

`object_id`  
The SNMP object id which precedes the wanted one.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns SNMP object value on success or **`FALSE`** on error. In case of
an error, an E\_WARNING message is shown.

### 范例

**示例 \#1 Using <span class="function">snmpgetnext</span>**

``` php
<?php
$nameOfSecondInterface = snmpgetnetxt('localhost', 'public', 'IF-MIB::ifName.1';
?>
```

### 参见

-   <span class="function">snmpget</span>
-   <span class="function">snmpwalk</span>

snmprealwalk
============

返回指定的所有对象，包括它们各自的对象 ID

### 说明

<span class="type">array</span> <span
class="methodname">snmprealwalk</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`<span class="initializer"> =
1000000</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`<span class="initializer"> =
5</span></span> \]\] )

The <span class="function">snmprealwalk</span> function is used to
traverse over a number of SNMP objects starting from `object_id` and
return not only their values but also their object ids.

### 参数

`host`  
The hostname of the SNMP agent (server).

`community`  
The read community.

`object_id`  
The SNMP object id which precedes the wanted one.

`timeout`  
The number of microseconds until the first timeout.

`retries`  
The number of times to retry if timeouts occur.

### 返回值

Returns an associative array of the SNMP object ids and their values on
success or **`FALSE`** on error. In case of an error, an E\_WARNING
message is shown.

### 范例

**示例 \#1 Using <span class="function">snmprealwalk</span>**

``` php
<?php
 print_r(snmprealwalk("localhost", "public", "IF-MIB::ifName"));
?>
```

The above will output something like:

         
        Array
          (
          [IF-MIB::ifName.1] => STRING: lo
          [IF-MIB::ifName.2] => STRING: eth0
          [IF-MIB::ifName.3] => STRING: eth2
          [IF-MIB::ifName.4] => STRING: sit0
          [IF-MIB::ifName.5] => STRING: sixxs
        )

### 参见

-   <span class="function">snmpwalk</span>

snmpset
=======

设置一个 SNMP 对象

### 说明

<span class="type">bool</span> <span class="methodname">snmpset</span> (
<span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">string</span> `$community`</span> , <span
class="methodparam"><span class="type">string</span> `$object_id`</span>
, <span class="methodparam"><span class="type">string</span>
`$type`</span> , <span class="methodparam"><span
class="type">mixed</span> `$value`</span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$retries`</span> \]\] )

设置指定的 SNMP 对象的值，成功返回 **`TRUE`**，错误则返回 **`FALSE`**。

函数 <span class="function">snmpset</span> 用于设置由 `object_id` 指定的
SNMP 对象的值。`hostname` 指定 SNMP 代理，而 `community`
参数指定具有读权限的域。

snmpwalk
========

从代理返回所有的 SNMP 对象

### 说明

<span class="type">array</span> <span class="methodname">snmpwalk</span>
( <span class="methodparam"><span class="type">string</span>
`$hostname`</span> , <span class="methodparam"><span
class="type">string</span> `$community`</span> , <span
class="methodparam"><span class="type">string</span> `$object_id`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$timeout`</span> \[, <span class="methodparam"><span
class="type">int</span> `$retries`</span> \]\] )

返回由 `object_id` 作为根的 SNMP 对象值所组成的数组，错误则返回
**`FALSE`**。

<span class="function">snmpwalk</span> 函数是用来读取所有由 `hostname`
指定的 SNMP 代理的值。`Community` 指定该代理中具有读权限的域。一个为
**`NULL`** 的 `object_id` 将被看作 SNMP
对象树的根，而在此树下的所有对象将作为一个数组被返回。如果指定了
`object_id`，则返回所有在 `object_id` 下的 SNMP 对象。

``` php
<?php
$a = snmpwalk("127.0.0.1", "public", ""); 
?>
```

上边的函数调用将从运行于本机的 SNMP 代理那里返回所有的 SNMP
对象。可使用循环遍历这些值。

``` php
<?php
foreach ($a as $val) {
    echo "$val\n";
}
?>
```

snmpwalkoid
===========

查询关于网络实体的信息树

### 说明

<span class="type">array</span> <span
class="methodname">snmpwalkoid</span> ( <span class="methodparam"><span
class="type">string</span> `$hostname`</span> , <span
class="methodparam"><span class="type">string</span> `$community`</span>
, <span class="methodparam"><span class="type">string</span>
`$object_id`</span> \[, <span class="methodparam"><span
class="type">int</span> `$timeout`</span> \[, <span
class="methodparam"><span class="type">int</span> `$retries`</span> \]\]
)

返回一个包含对象 id 及它们各自对象值的关联数组，这些对象以 `object_id`
作为根，错误则返回 **`FALSE`**。

<span class="function">snmpwalkoid</span> 用于从 `hostname` 所指定的
SNMP 代理那里读取所有对象 id 及它们各自的值。`community`
指定对于该代理有读权限的域。一个为 **`NULL`** 的 `object_id` 将被看作
SNMP 对象树的根，而在此树下的所有对象将作为一个数组被返回。如果指定了
`object_id`，则返回所有在 `object_id` 下的 SNMP 对象。

<span class="function">snmpwalkoid</span> 和 <span
class="function">snmpwalk</span>
的同时存在出于历史原因。提供两个函数是为了向后兼容。

``` php
<?php
$a = snmpwalkoid("127.0.0.1", "public", ""); 
?>
```

上边的函数调用将从运行于本机的 SNMP 代理那里返回所有的 SNMP
对象。可使用循环遍历这些值。

``` php
<?php
for (reset($a); $i = key($a); next($a)) {
    echo "$i: $a[$i]<br />\n";
}
?>
```

**目录**

-   [snmp\_get\_quick\_print](/ref/snmp.html#snmp_get_quick_print) —
    返回 UCD 库中 quick\_print 设置的当前值
-   [snmp\_get\_valueretrieval](/ref/snmp.html#snmp_get_valueretrieval)
    — Return the method how the SNMP values will be returned
-   [snmp\_read\_mib](/ref/snmp.html#snmp_read_mib) — Reads and parses a
    MIB file into the active MIB tree
-   [snmp\_set\_enum\_print](/ref/snmp.html#snmp_set_enum_print) —
    Return all values that are enums with their enum value instead of
    the raw integer
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
    objects including their respective object ID within the specified
    one
-   [snmp2\_set](/ref/snmp.html#snmp2_set) — Set the value of an SNMP
    object
-   [snmp2\_walk](/ref/snmp.html#snmp2_walk) — Fetch all the SNMP
    objects from an agent
-   [snmp3\_get](/ref/snmp.html#snmp3_get) — Fetch an SNMP object
-   [snmp3\_getnext](/ref/snmp.html#snmp3_getnext) — Fetch the SNMP
    object which follows the given object id
-   [snmp3\_real\_walk](/ref/snmp.html#snmp3_real_walk) — Return all
    objects including their respective object ID within the specified
    one
-   [snmp3\_set](/ref/snmp.html#snmp3_set) — Set the value of an SNMP
    object
-   [snmp3\_walk](/ref/snmp.html#snmp3_walk) — Fetch all the SNMP
    objects from an agent
-   [snmpget](/ref/snmp.html#snmpget) — 获取一个 SNMP 对象
-   [snmpgetnext](/ref/snmp.html#snmpgetnext) — Fetch the SNMP object
    which follows the given object id
-   [snmprealwalk](/ref/snmp.html#snmprealwalk) —
    返回指定的所有对象，包括它们各自的对象 ID
-   [snmpset](/ref/snmp.html#snmpset) — 设置一个 SNMP 对象
-   [snmpwalk](/ref/snmp.html#snmpwalk) — 从代理返回所有的 SNMP 对象
-   [snmpwalkoid](/ref/snmp.html#snmpwalkoid) — 查询关于网络实体的信息树
