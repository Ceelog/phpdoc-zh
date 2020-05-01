范例
====

**目录**

-   [wddx examples](/wddx/examples.html#wddx%20examples)

wddx examples
-------------

All the functions that serialize variables use the first element of an
array to determine whether the array is to be serialized into an array
or structure. If the first element has string key, then it is serialized
into a structure, otherwise, into an array.

**示例 \#1 Serializing a single value with WDDX**

``` php
<?php
echo wddx_serialize_value("PHP to WDDX packet example", "PHP packet");
?>
```

This example will produce:

    <wddxPacket version='1.0'><header comment='PHP packet'/><data>
    <string>PHP to WDDX packet example</string></data></wddxPacket>

**示例 \#2 Using incremental packets with WDDX**

``` php
<?php
$pi = 3.1415926;
$packet_id = wddx_packet_start("PHP");
wddx_add_vars($packet_id, "pi");

/* Suppose $cities came from database */
$cities = array("Austin", "Novato", "Seattle");
wddx_add_vars($packet_id, "cities");

$packet = wddx_packet_end($packet_id);
echo $packet;
?>
```

This example will produce:

    <wddxPacket version='1.0'><header comment='PHP'/><data><struct>
    <var name='pi'><number>3.1415926</number></var><var name='cities'>
    <array length='3'><string>Austin</string><string>Novato</string>
    <string>Seattle</string></array></var></struct></data></wddxPacket>

> **Note**:
>
> If you want to serialize non-ASCII characters you have to convert your
> data to UTF-8 first (see <span class="function">utf8\_encode</span>
> and <span class="function">iconv</span>).
