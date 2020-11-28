rrd\_create
===========

Creates rrd database file

### 说明

<span class="type">bool</span> <span
class="methodname">rrd\_create</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Creates the rdd database file.

### 参数

`filename`  
Filename for newly created rrd file.

`options`  
Options for rrd create - list of strings. See man page of rrd create for
whole list of options.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

rrd\_error
==========

Gets latest error message

### 说明

<span class="type">string</span> <span
class="methodname">rrd\_error</span> ( <span
class="methodparam">void</span> )

Returns latest global rrd error message.

### 参数

此函数没有参数。

### 返回值

Latest error message.

rrd\_fetch
==========

Fetch the data for graph as array

### 说明

<span class="type">array</span> <span
class="methodname">rrd\_fetch</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Gets data for graph output from RRD database file as array. This
function has same result as <span class="function">rrd\_graph</span>,
but fetched data are returned as array, no image file is created.

### 参数

`filename`  
RRD database file name.

`options`  
Array of options for resolution specification.

### 返回值

Returns information about retrieved graph data.

rrd\_first
==========

Gets the timestamp of the first sample from rrd file

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">rrd\_first</span> ( <span class="methodparam"><span
class="type">string</span> `$file`</span> \[, <span
class="methodparam"><span class="type">int</span> `$raaindex`<span
class="initializer"> = 0</span></span> \] )

Returns the first data sample from the specified RRA of the RRD file.

### 参数

`file`  
RRD database file name.

`raaindex`  
The index number of the RRA that is to be examined. Default value is 0.

### 返回值

Integer number of unix timestamp, **`FALSE`** if some error occurs.

rrd\_graph
==========

Creates image from a data

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">rrd\_graph</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Creates image for a particular data from RRD file.

### 参数

`filename`  
The filename to output the graph to. This will generally end in either
*.png*, *.svg* or *.eps*, depending on the format you want to output.

`options`  
Options for generating image. See man page of rrd graph for all possible
options. All options (data definitions, variable defintions, etc.) are
allowed.

### 返回值

Array with information about generated image is returned, **`FALSE`**
when error occurs.

rrd\_info
=========

Gets information about rrd file

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">rrd\_info</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

Returns information about particular RRD database file.

### 参数

`file`  
RRD database file name.

### 返回值

Array with information about requsted RRD file, **`FALSE`** when error
occurs.

rrd\_last
=========

Gets unix timestamp of the last sample

### 说明

<span class="type">int</span> <span class="methodname">rrd\_last</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> )

Returns the UNIX timestamp of the most recent update of the RRD
database.

### 参数

`filename`  
RRD database file name.

### 返回值

Integer as unix timestamp of the most recent data from the RRD database.

rrd\_lastupdate
===============

Gets information about last updated data

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">rrd\_lastupdate</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Gets array of the UNIX timestamp and the values stored for each date in
the most recent update of the RRD database file.

### 参数

`file`  
RRD database file name.

### 返回值

Array of information about last update, **`FALSE`** when error occurs.

rrd\_restore
============

Restores the RRD file from XML dump

### 说明

<span class="type">bool</span> <span
class="methodname">rrd\_restore</span> ( <span class="methodparam"><span
class="type">string</span> `$xml_file`</span> , <span
class="methodparam"><span class="type">string</span> `$rrd_file`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

Restores the RRD file from the XML dump.

### 参数

`xml_file`  
XML filename with the dump of the original RRD database file.

`rrd_file`  
Restored RRD database file name.

`options`  
Array of options for restoring. See man page for rrd restore.

### 返回值

Returns **`TRUE`** on success, **`FALSE`** otherwise.

rrd\_tune
=========

Tunes some RRD database file header options

### 说明

<span class="type">bool</span> <span class="methodname">rrd\_tune</span>
( <span class="methodparam"><span class="type">string</span>
`$filename`</span> , <span class="methodparam"><span
class="type">array</span> `$options`</span> )

Change some options in the RRD dabase header file. E.g. renames the
source for the data etc.

### 参数

`filename`  
RRD database file name.

`options`  
Options with RRD database file properties which will be changed. See rrd
tune man page for details.

### 返回值

Returns **`TRUE`** on success, **`FALSE`** otherwise.

rrd\_update
===========

Updates the RRD database

### 说明

<span class="type">bool</span> <span
class="methodname">rrd\_update</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">array</span> `$options`</span> )

Updates the RRD database file. The input data is time interpolated
according to the properties of the RRD database file.

### 参数

`filename`  
RRD database file name. This database will be updated.

`options`  
Options for updating the RRD database. This is list of strings. See man
page of rrd update for whole list of options.

### 返回值

Returns **`TRUE`** on success, **`FALSE`** when error occurs.

rrd\_version
============

Gets information about underlying rrdtool library

### 说明

<span class="type">string</span> <span
class="methodname">rrd\_version</span> ( <span
class="methodparam">void</span> )

Returns information about underlying rrdtool library.

### 参数

此函数没有参数。

### 返回值

String with rrdtool version number e.g. "1.4.3".

rrd\_xport
==========

Exports the information about RRD database

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">rrd\_xport</span> ( <span class="methodparam"><span
class="type">array</span> `$options`</span> )

Exports the information about RRD database file. This data can be
converted to XML file via user space PHP script and then restored back
as RRD database file.

### 参数

`options`  
Array of options for the export, see rrd xport man page.

### 返回值

Array with information about RRD database file, **`FALSE`** when error
occurs.

rrdc\_disconnect
================

Close any outstanding connection to rrd caching daemon

### 说明

<span class="type">void</span> <span
class="methodname">rrdc\_disconnect</span> ( <span
class="methodparam">void</span> )

Close any outstanding connection to rrd caching daemon.

This function is automatically called when the whole PHP process is
terminated. It depends on used SAPI. For example, it's called
automatically at the end of command line script.

It's up user whether he wants to call this function at the end of every
request or otherwise.

### 参数

此函数没有参数。

### 返回值

没有返回值。

**目录**

-   [rrd\_create](/ref/rrd.html#rrd_create) — Creates rrd database file
-   [rrd\_error](/ref/rrd.html#rrd_error) — Gets latest error message
-   [rrd\_fetch](/ref/rrd.html#rrd_fetch) — Fetch the data for graph as
    array
-   [rrd\_first](/ref/rrd.html#rrd_first) — Gets the timestamp of the
    first sample from rrd file
-   [rrd\_graph](/ref/rrd.html#rrd_graph) — Creates image from a data
-   [rrd\_info](/ref/rrd.html#rrd_info) — Gets information about rrd
    file
-   [rrd\_last](/ref/rrd.html#rrd_last) — Gets unix timestamp of the
    last sample
-   [rrd\_lastupdate](/ref/rrd.html#rrd_lastupdate) — Gets information
    about last updated data
-   [rrd\_restore](/ref/rrd.html#rrd_restore) — Restores the RRD file
    from XML dump
-   [rrd\_tune](/ref/rrd.html#rrd_tune) — Tunes some RRD database file
    header options
-   [rrd\_update](/ref/rrd.html#rrd_update) — Updates the RRD database
-   [rrd\_version](/ref/rrd.html#rrd_version) — Gets information about
    underlying rrdtool library
-   [rrd\_xport](/ref/rrd.html#rrd_xport) — Exports the information
    about RRD database
-   [rrdc\_disconnect](/ref/rrd.html#rrdc_disconnect) — Close any
    outstanding connection to rrd caching daemon
