geoip\_asnum\_by\_name
======================

获取自治系统号(ASN)

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_asnum\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_asnum\_by\_name</span> 函数将会返回和 IP
地址相关联的自治系统号(ASN)。

### 参数

`hostname`  
主机的 IP 地址。

### 返回值

如果成功将会返回自治系统号，如果在数据库中未找到相关信息则返回
**`false`** 。

### 范例

**示例 \#1 <span
class="function">geoip\_asnum\_by\_name</span>函数的范例：**

以下代码将会输出 www.example.com 域名的 ASN。

``` php
<?php
$asn = geoip_asnum_by_name('www.example.com');

if ($asn) {
    echo 'The ASN is: ' $asn;
}
?>
```

以上例程会输出：

    The ASN is: AS15133 EdgeCast Networks, Inc

geoip\_continent\_code\_by\_name
================================

获取七大洲的大写字母简称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_continent\_code\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_continent\_code\_by\_name</span>
函数将会返回主机或者IP地址相对应的七大洲大写字母简称。

### 参数

`hostname`  
所要定位的主机或IP地址。

### 返回值

成功，返回两个大写字母组成的七大洲简称字符串,
如果在数据库中未找到相关信息则返回 **`false`** 。

| Code | 洲名   |
|------|--------|
| *AF* | 非洲   |
| *AN* | 南极洲 |
| *AS* | 亚洲   |
| *EU* | 欧洲   |
| *NA* | 北美洲 |
| *OC* | 大洋洲 |
| *SA* | 南美洲 |

### 范例

**示例 \#1 <span
class="function">geoip\_continent\_code\_by\_name</span>
函数的使用范例：**

以下代码将会打印 example.com 的定位信息。

``` php
<?php
$continent = geoip_continent_code_by_name('www.example.com');
if ($continent) {
    echo 'This host is located in: ' . $continent;
}
?>
```

以上例程会输出：

     This host is located in: NA

### 参见

-   <span class="function">geoip\_country\_code\_by\_name</span>

geoip\_country\_code\_by\_name
==============================

获取国家代码

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_country\_code\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_country\_code\_by\_name</span>
函数将会返回主机或者IP地址所在的国家代码。

### 参数

`hostname`  
定位的主机名或者IP地址。

### 返回值

成功，返回 ISO 定义的国家代码，如果在数据库中未找到相关信息则返回
**`false`** 。

### 范例

**示例 \#1 <span class="function">geoip\_country\_code\_by\_name</span>
函数的范例：**

以下代码将会打印 example.com 主机的定位信息。

``` php
<?php
$country = geoip_country_code_by_name('www.example.com');
if ($country) {
    echo 'This host is located in: ' . $country;
}
?>
```

以上例程会输出：

    This host is located in: US

### 注释

**Caution**

请点击
<a href="http://www.maxmind.com/en/iso3166" class="link external">» http://www.maxmind.com/en/iso3166</a>
来查看所有可能的返回值列表，包括特殊代码。

### 参见

-   <span class="function">geoip\_country\_code3\_by\_name</span>
-   <span class="function">geoip\_country\_name\_by\_name</span>

geoip\_country\_code3\_by\_name
===============================

获取三个字母组成的国家简称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_country\_code3\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_country\_code3\_by\_name</span>
函数返回由三个字母组成和主机或者 IP 相对应的国家代码。

### 参数

`hostname`  
定位所用的主机名或者 IP 地址。

### 返回值

成功，返回由三个字母组成的国家简称，如果在数据库中未找到相关信息则返回
**`false`** 。

### 范例

**示例 \#1 <span class="function">geoip\_country\_code3\_by\_name</span>
函数的使用范例：**

以下代码将会打印 example.com 主机的定位信息。

``` php
<?php
$country = geoip_country_code3_by_name('www.example.com');
if ($country) {
    echo 'This host is located in: ' . $country;
}
?>
```

以上例程会输出：

    This host is located in: USA

### 参见

-   <span class="function">geoip\_country\_code\_by\_name</span>
-   <span class="function">geoip\_country\_name\_by\_name</span>

geoip\_country\_name\_by\_name
==============================

获取国家的全称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_country\_name\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_country\_name\_by\_name</span>
函数返回主机或者 IP 地址所对应的国家名全称。

### 参数

`hostname`  
定位所用的主机或者 IP 地址。

### 返回值

成功，返回国家全称，如果在数据库中未找到相关信息则返回 **`false`** 。

### 范例

**示例 \#1 <span class="function">geoip\_country\_name\_by\_name</span>
函数的使用范例：**

以下代码将会打印 example.com 主机的定位信息。

``` php
<?php
$country = geoip_country_name_by_name('www.example.com');
if ($country) {
    echo 'This host is located in: ' . $country;
}
?>
```

以上例程会输出：

     This host is located in: United States

### 参见

-   <span class="function">geoip\_country\_code\_by\_name</span>
-   <span class="function">geoip\_country\_code3\_by\_name</span>

geoip\_database\_info
=====================

获取 GeoIP 数据库的信息

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_database\_info</span> (\[ <span
class="methodparam"><span class="type">int</span> `$database`<span
class="initializer"> = GEOIP\_COUNTRY\_EDITION</span></span> \] )

<span class="function">geoip\_database\_info</span> 函数返回 GeoIP
数据库版本的信息。

如果无参调用该函数，则返回 GeoIP 免费国家版的版本信息。

### 参数

`database`  
该变量的类型为整型。你可以使用该扩展的<a href="/geoip/constants.html" class="link">预定义常量</a>(类似:
GEOIP\_\*\_EDITION)。

### 返回值

如果成功，返回数据库的版本信息，错误则返回**`null`** 。

### 范例

**示例 \#1 <span class="function">geoip\_database\_info</span>
函数的使用范例：**

以下代码将会输出数据库的相关信息。

``` php
<?php
print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

以上例程会输出：

    GEO-106FREE 20060801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved

geoip\_db\_avail
================

GeoIP 数据库是否可用

### 说明

<span class="type">bool</span> <span
class="methodname">geoip\_db\_avail</span> ( <span
class="methodparam"><span class="type">int</span> `$database`</span> )

<span class="function">geoip\_db\_avail</span> 函数返回 GeoI
P数据库是否可以在磁盘上打开并且可用。

该函数不能用来判断是否是个合适的数据库，除非这个数据库可读。

### 参数

`database`  
变量类型为整型。你可以使用该扩展的<a href="/geoip/constants.html" class="link">预定义常量</a>(比如:
GEOIP\_\*\_EDITION)。

### 返回值

如果存在则返回 **`true`** , 未找到则返回 **`false`** , 错误则返回
**`null`** 。

### 范例

**示例 \#1 <span class="function">geoip\_db\_avail</span>
函数的使用范例：**

以下代码将会输出当前数据库的版本信息。

``` php
<?php

if (geoip_db_avail(GEOIP_COUNTRY_EDITION))
    print geoip_database_info(GEOIP_COUNTRY_EDITION);
?>
```

以上例程会输出：

    GEO-106FREE 20080801 Build 1 Copyright (c) 2006 MaxMind LLC All Rights Reserved

geoip\_db\_filename
===================

返回 GeoIP 数据库相对应的文件名

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_db\_filename</span> ( <span
class="methodparam"><span class="type">int</span> `$database`</span> )

<span class="function">geoip\_db\_filename</span> 函数将会返回和 GeoIP
数据库相对应的文件名。

这个函数不会判别文件是否存在在磁盘上，只会表明拓展库在哪里查找数据库。

### 参数

`database`  
该参数为整型。你可以使用该扩展的<a href="/geoip/constants.html" class="link">预定义常量</a>
(比如: GEOIP\_\*\_EDITION)。

### 返回值

成功则返回相对应的数据库文件名，错误则返回**`null`** 。

### 范例

**示例 \#1 <span
class="function">geoip\_db\_filename</span>函数的使用范例：**

如下代码将会打印数据库相对应的文件名。

``` php
<?php

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

以上例程会输出：

    /usr/share/GeoIP/GeoIP.dat

geoip\_db\_get\_all\_info
=========================

返回所有 GeoIP 数据库类型的详细信息

### 说明

<span class="type">array</span> <span
class="methodname">geoip\_db\_get\_all\_info</span> ( <span
class="methodparam">void</span> )

<span class="function">geoip\_db\_get\_all\_info</span>
函数将会返回包含所有 GeoIP 数据库类型详细信息的多维数组

即使没有安装数据库，这个函数依旧可用。它将会列出数据库是否可用。

返回的关联数组，各键值所代表的含义如下：

-   <span class="simpara"> "available" -- 布尔值,
    表示数据库是否可用(请参考 <span
    class="function">geoip\_db\_avail</span>) </span>
-   <span class="simpara"> "description" -- 数据库的描述 </span>
-   <span class="simpara"> "filename" -- 磁盘上的数据库文件名(请参考
    <span class="function">geoip\_db\_filename</span>) </span>

### 返回值

返回一个关联数组。

### 范例

**示例 \#1 <span class="function">geoip\_db\_get\_all\_info</span>
使用范例：**

以下代码将会打印包含所有信息的数组。

``` php
<?php
$infos = geoip_db_get_all_info();
if (is_array($infos)) {
    var_dump($infos);
}
?>
```

以上例程会输出：

    array(11) {
      [1]=>
      array(3) {
        ["available"]=>
        bool(true)
        ["description"]=>
        string(21) "GeoIP Country Edition"
        ["filename"]=>
        string(32) "/usr/share/GeoIP/GeoIP.dat"
      }

    [ ... ]

      [11]=>
      array(3) {
        ["available"]=>
        bool(false)
        ["description"]=>
        string(25) "GeoIP Domain Name Edition"
        ["filename"]=>
        string(38) "/usr/share/GeoIP/GeoIPDomain.dat"
      }
    }

**示例 \#2 <span class="function">geoip\_db\_get\_all\_info</span>
使用范例：**

你可以使用不同的常量作为键来获取部分信息。

``` php
<?php
$infos = geoip_db_get_all_info();
if ($infos[GEOIP_COUNTRY_EDITION]['available']) {
    echo $infos[GEOIP_COUNTRY_EDITION]['description'];
}
?>
```

以上例程会输出：

    GeoIP Country Edition

geoip\_domain\_by\_name
=======================

获取二级域名

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_domain\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_domain\_by\_name</span>
函数将会返回和主机或者 IP 地址相关联的二级域名。

当前该函数只对购买了商业 GeoIP
域名版本的用户是可用的。如果没有该版本的数据库，使用该函数时将会抛出一个警告。

### 参数

`hostname`  
主机名或者 IP 地址。

### 返回值

成功，返回域名，如果在数据库中未找到信息则返回 **`false`** 。

### 范例

**示例 \#1 一个 <span class="function">geoip\_domain\_by\_name</span>
使用范例：**

以下代码将会输出和 IP 61.106.139.1相关联的域名。

``` php
<?php
$domain = geoip_domain_by_name('61.106.139.1');

if ($domain) {
    echo 'The domain is: '. $domain;
}

?>
```

以上例程会输出：

    The domain is: von.co.kr

geoip\_id\_by\_name
===================

获取网络连接类型

### 说明

<span class="type">int</span> <span
class="methodname">geoip\_id\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_id\_by\_name</span>
函数将会返回和主机名或者 IP 地址相对应的网络连接类型。

函数返回值是数字可以和以下常量对照：

-   <span class="simpara"> GEOIP\_UNKNOWN\_SPEED </span>
-   <span class="simpara"> GEOIP\_DIALUP\_SPEED </span>
-   <span class="simpara"> GEOIP\_CABLEDSL\_SPEED </span>
-   <span class="simpara"> GEOIP\_CORPORATE\_SPEED </span>

### 参数

`hostname`  
要查找连接类型的主机或者 IP 地址。

### 返回值

返回连接类型。

### 范例

**示例 \#1 一个 <span class="function">geoip\_id\_by\_name</span>
使用范例：**

以下将会输出 example.com 主机的连接类型。

``` php
<?php
$netspeed = geoip_id_by_name('www.example.com');

echo 'The connection type is ';

switch ($netspeed) {
    case GEOIP_DIALUP_SPEED:
        echo 'dial-up';
        break;
    case GEOIP_CABLEDSL_SPEED:
        echo 'cable or DSL';
        break;
    case GEOIP_CORPORATE_SPEED:
        echo 'corporate';
        break;
    case GEOIP_UNKNOWN_SPEED:
    default:
        echo 'unknown';
}
?>
```

以上例程会输出：

    The connection type is corporate

geoip\_isp\_by\_name
====================

获取 ISP (网络服务提供商)的名称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_isp\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_isp\_by\_name</span> 函数将会返回 IP
地址所归属的网络服务提供商(ISP)的名称。

目前，该函数只对购买了商业 GeoIP ISP
版本的用户可用，否则将会抛出一个警告！

### 参数

`hostname`  
主机或者 IP 地址。

### 返回值

成功，则返回 ISP 名称，未找到相关信息则返回 **`false`** 。

### 范例

**示例 \#1 一个 <span class="function">geoip\_isp\_by\_name</span>
使用范例：**

以下代码将会输出 example.com 主机的 ISP 名称。

``` php
<?php
$isp = geoip_isp_by_name('www.example.com');
if ($isp) {
    echo 'This host IP is from ISP: ' . $isp;
}
?>
```

以上例程会输出：

    This host IP is from ISP: ICANN c/o Internet Assigned Numbers Authority

geoip\_netspeedcell\_by\_name
=============================

获取网络连接速度

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_netspeedcell\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_netspeedcell\_by\_name</span>
函数将会返回主机或者 IP 地址对应的网络连接类型和速度。

该函数只有在 GeoIP 1.4.8 版本以上才能使用。

目前，该函数只对购买了商业 GeoIP NetSpeedCell
版本的用户可用，否则将会抛出一个警告！

返回值为字符串，结果集如下：

-   <span class="simpara"> Cable/DSL </span>
-   <span class="simpara"> Dialup </span>
-   <span class="simpara"> Cellular </span>
-   <span class="simpara"> Corporate </span>

### 参数

`hostname`  
主机名或者 IP 地址。

### 返回值

成功，返回连接速度，未找到相关信息则返回 **`false`** 。

### 范例

**示例 \#1 一个 <span
class="function">geoip\_netspeedcell\_by\_name</span> 使用范例：**

以下代码将会输出 example.com 主机的连接速度。

``` php
<?php
$netspeed = geoip_netspeedcell_by_name('www.example.com');

if ($netspeed) {
    echo 'The connection type is: '. $netspeed;
}
?>
```

以上例程会输出：

    The connection type is: Corporate

geoip\_org\_by\_name
====================

获取机构的名称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_org\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_org\_by\_name</span> 函数将会返回 IP
地址所分配的机构名称。

目前，该函数只对购买了商业 GeoIP Organization， ISP 或者 AS
版本的用户可用，否则将会抛出一个警告！

### 参数

`hostname`  
主机名或者 IP 地址。

### 返回值

成功， 返回组织的名称，未找到相关信息则返回 **`false`** 。

### 范例

**示例 \#1 一个 <span class="function">geoip\_org\_by\_name</span>
使用范例：**

以下代码将会打印 example.com 主机的所有者。

``` php
<?php
$org = geoip_org_by_name('www.example.com');
if ($org) {
    echo 'This host IP is allocated to: ' . $org;
}
?>
```

以上例程会输出：

    This host IP is allocated to: ICANN c/o Internet Assigned Numbers Authority

geoip\_record\_by\_name
=======================

返回 GeoIP 数据库中详细的城市信息

### 说明

<span class="type">array</span> <span
class="methodname">geoip\_record\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_record\_by\_name</span>
函数将会返回主机或者 IP 地址所对应的记录信息。

该函数在 GeoLite City 版本和商业 GeoIP City 版本中可用。
版本不对的话，将会抛出一个警告。

返回的关联数组不同的键名对应如下：

-   <span class="simpara"> "continent\_code" --
    由两个字符组成的洲简称。(要求 GeoIP 的库版本是1.0.4以上) </span>
-   <span class="simpara"> "country\_code" --
    由2个字母组成的国家简称。(参见 <span
    class="function">geoip\_country\_code\_by\_name</span>) </span>
-   <span class="simpara"> "country\_code3" --
    由三个字母组成的国家简称。(参见 <span
    class="function">geoip\_country\_code3\_by\_name</span>) </span>
-   <span class="simpara"> "country\_name" -- 国家名称 (参见 <span
    class="function">geoip\_country\_name\_by\_name</span>) </span>
-   <span class="simpara"> "region" -- 地区代码 (比如: CA 对应
    California) </span>
-   <span class="simpara"> "city" -- 城市名称。 </span>
-   <span class="simpara"> "postal\_code" -- 邮编，FSA 或者 Zip 编码。
    </span>
-   <span class="simpara"> "latitude" -- 有符号的双精度纬度。 </span>
-   <span class="simpara"> "longitude" -- 有符号的双精度经度。 </span>
-   <span class="simpara"> "dma\_code" -- 指定市场区号
    (只支持美国和加拿大) </span>
-   <span class="simpara"> "area\_code" -- PSTN
    （公共交换电话网络）地区代码。 (比如: 212) </span>

### 参数

`hostname`  
所要查找的主机或者 IP 地址。

### 返回值

成功，返回关联数组，未找到相关信息则返回 **`false`** 。

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 1.0.4 | 给 GeoIP 1.4.4及以上版本的库添加 continent\_code 字段。 |
| 1.0.3 | 添加 country\_code3 和 country\_name 字段。             |

### 范例

**示例 \#1 <span class="function">geoip\_record\_by\_name</span>
例子：**

以下例程将会输出包含 example.com 主机记录的数组。

``` php
<?php
$record = geoip_record_by_name('www.example.com');
if ($record) {
    print_r($record);
}
?>
```

以上例程会输出：

    Array
    (
        [continent_code] => NA
        [country_code] => US
        [country_code3] => USA
        [country_name] => United States
        [region] => CA
        [city] => Marina Del Rey
        [postal_code] => 
        [latitude] => 33.9776992798
        [longitude] => -118.435096741
        [dma_code] => 803
        [area_code] => 310
    )

geoip\_region\_by\_name
=======================

获取国家和地区代码

### 说明

<span class="type">array</span> <span
class="methodname">geoip\_region\_by\_name</span> ( <span
class="methodparam"><span class="type">string</span> `$hostname`</span>
)

<span class="function">geoip\_region\_by\_name</span>
函数将会返回与主机或者 IP 地址相关的国家和地区代码。

该函数只对购买了商业 GeoIP Region 版本的用户可用。否则将会抛出一个警告！

所返回的关联数组的各字段具体含义如下：

-   <span class="simpara"> "country\_code" --
    由两个字母组成的国家代码(参见 <span
    class="function">geoip\_country\_code\_by\_name</span>) </span>
-   <span class="simpara"> "region" -- 地区代码。 (比如: CA 对应
    California) </span>

### 参数

`hostname`  
查找的主机或者 IP 地址。

### 返回值

成功，返回关联数组， 如果信息未找到则返回 **`false`**。

### 范例

**示例 \#1 <span class="function">geoip\_region\_by\_name</span>
例子：**

以下例程将会打印对应 example.com 主机的包含国家和地区代码的关联数组。

``` php
<?php
$region = geoip_region_by_name('www.example.com');
if ($region) {
    print_r($region);
}
?>
```

以上例程会输出：

    Array
    (
        [country_code] => US
        [region] => CA
    )

geoip\_region\_name\_by\_code
=============================

返回给定的国家和地区代码组合所对应的地区名称

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_region\_name\_by\_code</span> ( <span
class="methodparam"><span class="type">string</span>
`$country_code`</span> , <span class="methodparam"><span
class="type">string</span> `$region_code`</span> )

<span class="function">geoip\_region\_name\_by\_code</span>
函数将会返回与给定的国家和地区代码组合相对应的地区名称。

在美国，地区代码是每个州对应的两个字母的缩写，而在加拿大，则是由两个字母组成的每个省的邮政编码。

在世界其他地区，GeoIP使用 FIPS
给定的10到4位的代码来表示各地区。你可以点击以下连接
<a href="http://www.maxmind.com/app/fips10_4" class="link external">» http://www.maxmind.com/app/fips10_4</a>
查看详细信息。

该函数只在 GeoIP 1.4.1版本以上的库才可用。并且结果集的数据来源是直接从
GeoIP 库中获取的，而不是从任何数据库中。

### 参数

`country_code`  
由两个字母组成的国家代码 (参见 <span
class="function">geoip\_country\_code\_by\_name</span>)

`region_code`  
由两个字母组成的地区代码 (参见 <span
class="function">geoip\_region\_by\_name</span>)

### 返回值

成功，返回地区名字，如果相关信息未找到则返回 **`false`** 。

### 范例

**示例 \#1 <span class="function">geoip\_region\_name\_by\_code</span>
使用美国和加拿大地区的范例。**

以下例程将会打印国家简称为 CA (加拿大)，地区简称为 QC (魁北克)的地区名：

``` php
<?php
$region = geoip_region_name_by_code('CA', 'QC');
if ($region) {
    echo 'Region name for CA/QC is: ' . $region;
}
?>
```

以上例程会输出：

    Region name for CA/QC is: Quebec

**示例 \#2 <span class="function">geoip\_region\_name\_by\_code</span>
使用 FIPS 代码的范例：**

以下例程将会打印国家简称为 JP (日本)地区代码为 01的地区名称。

``` php
<?php
$region = geoip_region_name_by_code('JP', '01');
if ($region) {
    echo 'Region name for JP/01 is: ' . $region;
}
?>
```

以上例程会输出：

    Region name for JP/01 is: Aichi

geoip\_setup\_custom\_directory
===============================

自定义 GeoIP 数据库的目录

### 说明

<span class="type">void</span> <span
class="methodname">geoip\_setup\_custom\_directory</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="function">geoip\_setup\_custom\_directory</span>
函数将会更改 GeoIP 数据库的默认目录。这个设置和直接在 php
配置文件中设置的<a href="/geoip/setup.html#" class="link">geoip.custom_directory</a>参数效果是一样的。

### 参数

`path`  
磁盘上 GeoIP 数据库的绝对路径。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">geoip\_setup\_custom\_directory</span>
例子：**

以下例程将会更改 GeoIP 默认数据库的路径。

``` php
<?php

geoip_setup_custom_directory('/some/other/path');

print geoip_db_filename(GEOIP_COUNTRY_EDITION);

?>
```

以上例程会输出：

    /some/other/path/GeoIP.dat

geoip\_time\_zone\_by\_country\_and\_region
===========================================

返回国家和地区的时区

### 说明

<span class="type">string</span> <span
class="methodname">geoip\_time\_zone\_by\_country\_and\_region</span> (
<span class="methodparam"><span class="type">string</span>
`$country_code`</span> \[, <span class="methodparam"><span
class="type">string</span> `$region_code`</span> \] )

<span
class="function">geoip\_time\_zone\_by\_country\_and\_region</span>
函数将会返回与国家或者地区相对应的时区。

在美国，地区代码是每个州对应的两个字母的缩写，而在加拿大，则是由两个字母组成的每个省的邮政编码。

在世界上其他地区，GeoIP 使用 FIPS
给定的10到4位的代码来表示各地区。你可以点击以下连接
<a href="http://www.maxmind.com/app/fips10_4" class="link external">» http://www.maxmind.com/app/fips10_4</a>
查看详细信息。

该函数只在 GeoIP 1.4.1版本以上的库才可用。并且结果集的数据来源是直接从
GeoIP 库中获取的，而不是从任何数据库中。

### 参数

`country_code`  
由两个字母组成的国家代码 (参见 <span
class="function">geoip\_country\_code\_by\_name</span>)

`region_code`  
由两个字母组成的地区代码 (参见 <span
class="function">geoip\_region\_by\_name</span>)

### 返回值

成功，返回地区名字，如果相关信息未找到则返回 **`false`** 。

### 范例

**示例 \#1 <span
class="function">geoip\_time\_zone\_by\_country\_and\_region</span>
使用美国和加拿大地区的范例：**

以下例程将会打印国家简称为 CA (加拿大)，地区简称为 QC (魁北克)的时区。

``` php
<?php
$timezone = geoip_time_zone_by_country_and_region('CA', 'QC');
if ($timezone) {
    echo 'Time zone for CA/QC is: ' . $timezone;
}
?>
```

以上例程会输出：

    Time zone for CA/QC is: America/Montreal

**示例 \#2 <span
class="function">geoip\_time\_zone\_by\_country\_and\_region</span> 使用
FIPS 代码的范例：**

以下例程将会打印国家简称为 JP (日本),地区代码为 01的时区。

``` php
<?php
$timezone = geoip_time_zone_by_country_and_region('JP', '01');
if ($timezone) {
    echo 'Time zone for JP/01 is: ' . $timezone;
}
?>
```

以上例程会输出：

    Time zone for JP/01 is: Asia/Tokyo

**目录**

-   [geoip\_asnum\_by\_name](/ref/geoip.html#geoip_asnum_by_name) —
    获取自治系统号(ASN)
-   [geoip\_continent\_code\_by\_name](/ref/geoip.html#geoip_continent_code_by_name)
    — 获取七大洲的大写字母简称
-   [geoip\_country\_code\_by\_name](/ref/geoip.html#geoip_country_code_by_name)
    — 获取国家代码
-   [geoip\_country\_code3\_by\_name](/ref/geoip.html#geoip_country_code3_by_name)
    — 获取三个字母组成的国家简称
-   [geoip\_country\_name\_by\_name](/ref/geoip.html#geoip_country_name_by_name)
    — 获取国家的全称
-   [geoip\_database\_info](/ref/geoip.html#geoip_database_info) — 获取
    GeoIP 数据库的信息
-   [geoip\_db\_avail](/ref/geoip.html#geoip_db_avail) — GeoIP
    数据库是否可用
-   [geoip\_db\_filename](/ref/geoip.html#geoip_db_filename) — 返回
    GeoIP 数据库相对应的文件名
-   [geoip\_db\_get\_all\_info](/ref/geoip.html#geoip_db_get_all_info) —
    返回所有 GeoIP 数据库类型的详细信息
-   [geoip\_domain\_by\_name](/ref/geoip.html#geoip_domain_by_name) —
    获取二级域名
-   [geoip\_id\_by\_name](/ref/geoip.html#geoip_id_by_name) —
    获取网络连接类型
-   [geoip\_isp\_by\_name](/ref/geoip.html#geoip_isp_by_name) — 获取 ISP
    (网络服务提供商)的名称
-   [geoip\_netspeedcell\_by\_name](/ref/geoip.html#geoip_netspeedcell_by_name)
    — 获取网络连接速度
-   [geoip\_org\_by\_name](/ref/geoip.html#geoip_org_by_name) —
    获取机构的名称
-   [geoip\_record\_by\_name](/ref/geoip.html#geoip_record_by_name) —
    返回 GeoIP 数据库中详细的城市信息
-   [geoip\_region\_by\_name](/ref/geoip.html#geoip_region_by_name) —
    获取国家和地区代码
-   [geoip\_region\_name\_by\_code](/ref/geoip.html#geoip_region_name_by_code)
    — 返回给定的国家和地区代码组合所对应的地区名称
-   [geoip\_setup\_custom\_directory](/ref/geoip.html#geoip_setup_custom_directory)
    — 自定义 GeoIP 数据库的目录
-   [geoip\_time\_zone\_by\_country\_and\_region](/ref/geoip.html#geoip_time_zone_by_country_and_region)
    — 返回国家和地区的时区
