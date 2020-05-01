iis\_add\_server
================

Creates a new virtual web server

### 说明

<span class="type">int</span> <span
class="methodname">iis\_add\_server</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> ,
<span class="methodparam"><span class="type">string</span>
`$comment`</span> , <span class="methodparam"><span
class="type">string</span> `$server_ip`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">string</span> `$host_name`</span>
, <span class="methodparam"><span class="type">int</span>
`$rights`</span> , <span class="methodparam"><span
class="type">int</span> `$start_server`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_get\_dir\_security
=======================

Gets Directory Security

### 说明

<span class="type">int</span> <span
class="methodname">iis\_get\_dir\_security</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_get\_script\_map
=====================

Gets script mapping on a virtual directory for a specific extension

### 说明

<span class="type">string</span> <span
class="methodname">iis\_get\_script\_map</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> , <span
class="methodparam"><span class="type">string</span>
`$script_extension`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_get\_server\_by\_comment
=============================

Return the instance number associated with the Comment

### 说明

<span class="type">int</span> <span
class="methodname">iis\_get\_server\_by\_comment</span> ( <span
class="methodparam"><span class="type">string</span> `$comment`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_get\_server\_by\_path
==========================

Return the instance number associated with the Path

### 说明

<span class="type">int</span> <span
class="methodname">iis\_get\_server\_by\_path</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

Each virtual server in IIS is associated with an instance number. <span
class="function">iis\_get\_server\_by\_path</span> finds the instance
number from the actual path to the root directory.

### 参数

`path`  
The path to the root directory

### 返回值

Returns the server instance number.

iis\_get\_server\_rights
========================

Gets server rights

### 说明

<span class="type">int</span> <span
class="methodname">iis\_get\_server\_rights</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_get\_service\_state
========================

Returns the state for the service defined by ServiceId

### 说明

<span class="type">int</span> <span
class="methodname">iis\_get\_service\_state</span> ( <span
class="methodparam"><span class="type">string</span>
`$service_id`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_remove\_server
===================

Removes the virtual web server indicated by ServerInstance

### 说明

<span class="type">int</span> <span
class="methodname">iis\_remove\_server</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_set\_app\_settings
=======================

Creates application scope for a virtual directory

### 说明

<span class="type">int</span> <span
class="methodname">iis\_set\_app\_settings</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> , <span
class="methodparam"><span class="type">string</span>
`$application_scope`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_set\_dir\_security
=======================

Sets Directory Security

### 说明

<span class="type">int</span> <span
class="methodname">iis\_set\_dir\_security</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> , <span
class="methodparam"><span class="type">int</span>
`$directory_flags`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_set\_script\_map
=====================

Sets script mapping on a virtual directory

### 说明

<span class="type">int</span> <span
class="methodname">iis\_set\_script\_map</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> , <span
class="methodparam"><span class="type">string</span>
`$script_extension`</span> , <span class="methodparam"><span
class="type">string</span> `$engine_path`</span> , <span
class="methodparam"><span class="type">int</span>
`$allow_scripting`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_set\_server\_rights
========================

Sets server rights

### 说明

<span class="type">int</span> <span
class="methodname">iis\_set\_server\_rights</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> , <span class="methodparam"><span
class="type">string</span> `$virtual_path`</span> , <span
class="methodparam"><span class="type">int</span>
`$directory_flags`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_start\_server
==================

Starts the virtual web server

### 说明

<span class="type">int</span> <span
class="methodname">iis\_start\_server</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_start\_service
===================

Starts the service defined by ServiceId

### 说明

<span class="type">int</span> <span
class="methodname">iis\_start\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$service_id`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_stop\_server
=================

Stops the virtual web server

### 说明

<span class="type">int</span> <span
class="methodname">iis\_stop\_server</span> ( <span
class="methodparam"><span class="type">int</span>
`$server_instance`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

iis\_stop\_service
==================

Stops the service defined by ServiceId

### 说明

<span class="type">int</span> <span
class="methodname">iis\_stop\_service</span> ( <span
class="methodparam"><span class="type">string</span>
`$service_id`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

**目录**

-   [iis\_add\_server](/ref/iisfunc.html#iis_add_server) — Creates a new
    virtual web server
-   [iis\_get\_dir\_security](/ref/iisfunc.html#iis_get_dir_security) —
    Gets Directory Security
-   [iis\_get\_script\_map](/ref/iisfunc.html#iis_get_script_map) — Gets
    script mapping on a virtual directory for a specific extension
-   [iis\_get\_server\_by\_comment](/ref/iisfunc.html#iis_get_server_by_comment)
    — Return the instance number associated with the Comment
-   [iis\_get\_server\_by\_path](/ref/iisfunc.html#iis_get_server_by_path)
    — Return the instance number associated with the Path
-   [iis\_get\_server\_rights](/ref/iisfunc.html#iis_get_server_rights)
    — Gets server rights
-   [iis\_get\_service\_state](/ref/iisfunc.html#iis_get_service_state)
    — Returns the state for the service defined by ServiceId
-   [iis\_remove\_server](/ref/iisfunc.html#iis_remove_server) — Removes
    the virtual web server indicated by ServerInstance
-   [iis\_set\_app\_settings](/ref/iisfunc.html#iis_set_app_settings) —
    Creates application scope for a virtual directory
-   [iis\_set\_dir\_security](/ref/iisfunc.html#iis_set_dir_security) —
    Sets Directory Security
-   [iis\_set\_script\_map](/ref/iisfunc.html#iis_set_script_map) — Sets
    script mapping on a virtual directory
-   [iis\_set\_server\_rights](/ref/iisfunc.html#iis_set_server_rights)
    — Sets server rights
-   [iis\_start\_server](/ref/iisfunc.html#iis_start_server) — Starts
    the virtual web server
-   [iis\_start\_service](/ref/iisfunc.html#iis_start_service) — Starts
    the service defined by ServiceId
-   [iis\_stop\_server](/ref/iisfunc.html#iis_stop_server) — Stops the
    virtual web server
-   [iis\_stop\_service](/ref/iisfunc.html#iis_stop_service) — Stops the
    service defined by ServiceId
