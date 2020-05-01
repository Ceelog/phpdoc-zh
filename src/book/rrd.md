RRDtool
=======

**目录**

-   [简介](/intro/rrd.html)
-   [安装／配置](/rrd/setup.html)
    -   [需求](/rrd/setup.html#需求)
    -   [安装](/rrd/setup.html#安装)
    -   [运行时配置](/rrd/setup.html#运行时配置)
    -   [资源类型](/rrd/setup.html#资源类型)
-   [预定义常量](/rrd/constants.html)
-   [范例](/rrd/examples.html)
    -   [Procedural PECL/rrd
        example](/rrd/examples.html#Procedural%20PECL/rrd%20example)
    -   [OOP PECL/rrd
        example](/rrd/examples.html#OOP%20PECL/rrd%20example)
-   [RRD 函数](/ref/rrd.html)
    -   [rrd\_create](/ref/rrd.html#rrd_create) — Creates rrd database
        file
    -   [rrd\_error](/ref/rrd.html#rrd_error) — Gets latest error
        message
    -   [rrd\_fetch](/ref/rrd.html#rrd_fetch) — Fetch the data for graph
        as array
    -   [rrd\_first](/ref/rrd.html#rrd_first) — Gets the timestamp of
        the first sample from rrd file
    -   [rrd\_graph](/ref/rrd.html#rrd_graph) — Creates image from a
        data
    -   [rrd\_info](/ref/rrd.html#rrd_info) — Gets information about rrd
        file
    -   [rrd\_last](/ref/rrd.html#rrd_last) — Gets unix timestamp of the
        last sample
    -   [rrd\_lastupdate](/ref/rrd.html#rrd_lastupdate) — Gets
        information about last updated data
    -   [rrd\_restore](/ref/rrd.html#rrd_restore) — Restores the RRD
        file from XML dump
    -   [rrd\_tune](/ref/rrd.html#rrd_tune) — Tunes some RRD database
        file header options
    -   [rrd\_update](/ref/rrd.html#rrd_update) — Updates the RRD
        database
    -   [rrd\_version](/ref/rrd.html#rrd_version) — Gets information
        about underlying rrdtool library
    -   [rrd\_xport](/ref/rrd.html#rrd_xport) — Exports the information
        about RRD database
    -   [rrdc\_disconnect](/ref/rrd.html#rrdc_disconnect) — Close any
        outstanding connection to rrd caching daemon
-   [RRDCreator](/class/rrdcreator.html) — The RRDCreator class
    -   [RRDCreator::addArchive](/class/rrdcreator.html#RRDCreator::addArchive)
        — Adds RRA - archive of data values for each data source
    -   [RRDCreator::addDataSource](/class/rrdcreator.html#RRDCreator::addDataSource)
        — Adds data source definition for RRD database
    -   [RRDCreator::\_\_construct](/class/rrdcreator.html#RRDCreator::__construct)
        — Creates new RRDCreator instance
    -   [RRDCreator::save](/class/rrdcreator.html#RRDCreator::save) —
        Saves the RRD database to a file
-   [RRDGraph](/class/rrdgraph.html) — The RRDGraph class
    -   [RRDGraph::\_\_construct](/class/rrdgraph.html#RRDGraph::__construct)
        — Creates new RRDGraph instance
    -   [RRDGraph::save](/class/rrdgraph.html#RRDGraph::save) — Saves
        the result of query into image
    -   [RRDGraph::saveVerbose](/class/rrdgraph.html#RRDGraph::saveVerbose)
        — Saves the RRD database query into image and returns the
        verbose information about generated graph
    -   [RRDGraph::setOptions](/class/rrdgraph.html#RRDGraph::setOptions)
        — Sets the options for rrd graph export
-   [RRDUpdater](/class/rrdupdater.html) — The RRDUpdater class
    -   [RRDUpdater::\_\_construct](/class/rrdupdater.html#RRDUpdater::__construct)
        — Creates new RRDUpdater instance
    -   [RRDUpdater::update](/class/rrdupdater.html#RRDUpdater::update)
        — Update the RRD database file

简介
----

Class for creation of RRD database file.

类摘要
------

**RRDCreator**

<span class="ooclass"> class **RRDCreator** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addArchive</span> ( <span
class="methodparam"><span class="type">string</span>
`$description`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addDataSource</span> ( <span
class="methodparam"><span class="type">string</span>
`$description`</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$startTime`</span> \[, <span class="methodparam"><span
class="type">int</span> `$step`<span class="initializer"> =
0</span></span> \]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">save</span> ( <span
class="methodparam">void</span> )

}

RRDCreator::addArchive
======================

Adds RRA - archive of data values for each data source

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RRDCreator::addArchive</span> ( <span
class="methodparam"><span class="type">string</span>
`$description`</span> )

Adds RRA definition by description of archive. Archive consists of a
number of data values or statistics for each of the defined data-sources
(DS). Data sources are defined by method <span
class="methodname">RRDCreator::addDataSource</span>. You need call this
method for each requested archive.

### 参数

`description`  
Definition of archive - RRA. This has same format as RRA definition in
rrd create command. See man page of rrd create for more details.

### 返回值

没有返回值。

RRDCreator::addDataSource
=========================

Adds data source definition for RRD database

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RRDCreator::addDataSource</span> ( <span
class="methodparam"><span class="type">string</span>
`$description`</span> )

RRD can accept input from several data sources (DS), e.g incoming and
outgoing traffic. This method adds data source by description. You need
call this method for each data source.

### 参数

`description`  
Definition of data source - DS. This has same format as DS definition in
rrd create command. See man page of rrd create for more details.

### 返回值

没有返回值。

RRDCreator::\_\_construct
=========================

Creates new <span class="classname">RRDCreator</span> instance

### 说明

<span class="modifier">public</span> <span
class="methodname">RRDCreator::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$startTime`</span> \[, <span class="methodparam"><span
class="type">int</span> `$step`<span class="initializer"> =
0</span></span> \]\] )

Creates new RRDCreator instance.

### 参数

`path`  
Path for newly created RRD database file.

`startTime`  
Time for the first value in RRD database. Parameter supports all formats
which are supported by rrd create call.

int`step`  
Base interval in seconds with which data will be fed into the RRD
database.

### 返回值

没有返回值。

RRDCreator::save
================

Saves the RRD database to a file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RRDCreator::save</span> ( <span
class="methodparam">void</span> )

Saves the RRD database into file, which name is defined by <span
class="methodname">RRDCreator::\_\_construct</span>.

### 参数

此函数没有参数。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

简介
----

Class for exporting data from RRD database to image file.

类摘要
------

**RRDGraph**

<span class="ooclass"> class **RRDGraph** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">save</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">saveVerbose</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

}

RRDGraph::\_\_construct
=======================

Creates new <span class="classname">RRDGraph</span> instance

### 说明

<span class="modifier">public</span> <span
class="methodname">RRDGraph::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

Creates new RRDGraph instance. This instance is responsible for
rendering the result of RRD database query into image.

### 参数

`path`  
Full path for the newly created image.

### 返回值

没有返回值。

RRDGraph::save
==============

Saves the result of query into image

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">RRDGraph::save</span> ( <span
class="methodparam">void</span> )

Saves the result of RRD database query into image defined by <span
class="methodname">RRDGraph::\_\_construct</span>.

### 参数

此函数没有参数。

### 返回值

Array with information about generated image is returned, **`FALSE`** if
error occurs.

RRDGraph::saveVerbose
=====================

Saves the RRD database query into image and returns the verbose
information about generated graph

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">RRDGraph::saveVerbose</span> ( <span
class="methodparam">void</span> )

Saves the RRD database query into image file defined by method <span
class="methodname">RRDGraph::\_\_construct</span> and returns the
verbose information about generated graph, if "-" is used as image
filename, image data are also returned in result array.

### 参数

此函数没有参数。

### 返回值

Array with detailed information about generated image is returned,
optionally with image data, **`FALSE`** if error occurs.

RRDGraph::setOptions
====================

Sets the options for rrd graph export

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">RRDGraph::setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$options`</span> )

### 参数

`options`  
List of options for the image generation from the RRD database file. It
can be list of strings or list of strings with keys for better
readability. Read the rrd graph man pages for list of available options.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="methodname">RRDGraph::setOptions</span>
example**

``` php
<?php
$graphObj->setOptions(array(
    "--start" => "920804400",
    "--end" => 920808000,
    "--vertical-label" => "m/s",
    "DEF:myspeed=$rrdFile:speed:AVERAGE",
    "CDEF:realspeed=myspeed,1000,*",
    "LINE2:realspeed#FF0000"
));
?>
```

**示例 \#2 Set multiple color options**

``` php
<?php
$graphObj->setOptions(array(
    "--start" => "920804400",
    "--end" => 920808000,
    "--vertical-label" => "m/s",
    "--color=BACK#00000000",
    "--color=GRID#00000000",
    "--color=MGRID#00000000",
    "DEF:myspeed=$rrdFile:speed:AVERAGE",
    "CDEF:realspeed=myspeed,1000,*",
    "LINE2:realspeed#FF0000"
));
?>
```

Don't use key value syntax for same rrd option. It looks more readable,
but it doesn't work.

``` php
<?php
$graphObj->setOptions(array(
    "--color" => "BACK#00000000",
    "--color" => "GRID#00000000",
    "--color" => "MGRID#00000000"
));
?>
```

In nature of php it's same as

``` php
<?php
$graphObj->setOptions(array(
    "--color" => "MGRID#00000000"
));
?>
```

简介
----

Class for updating RDD database file.

类摘要
------

**RRDUpdater**

<span class="ooclass"> class **RRDUpdater** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">update</span> ( <span class="methodparam"><span
class="type">array</span> `$values`</span> \[, <span
class="methodparam"><span class="type">string</span> `$time` <span
class="initializer"> = time()</span> </span> \] )

}

RRDUpdater::\_\_construct
=========================

Creates new <span class="classname">RRDUpdater</span> instance

### 说明

<span class="modifier">public</span> <span
class="methodname">RRDUpdater::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

Creates new RRDUpdater instance. This instance is responsible for
updating the RRD database file.

### 参数

`path`  
Filesystem path for RRD database file, which will be updated.

### 返回值

没有返回值。

RRDUpdater::update
==================

Update the RRD database file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">RRDUpdater::update</span> ( <span
class="methodparam"><span class="type">array</span> `$values`</span> \[,
<span class="methodparam"><span class="type">string</span> `$time` <span
class="initializer"> = time()</span> </span> \] )

Updates the RRD file defined via <span
class="methodname">RRDUpdater::\_\_construct</span>. The file is updated
with a specific values.

### 参数

`values`  
Data for update. Key is data source name.

`time`  
Time value for updating the RRD with a particulat data. Default value is
current time.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 错误／异常

Throws a <span class="classname">Exception</span> on error.

### 范例

**示例 \#1 <span class="methodname">RRDUpdater::update</span> examples**

``` php
<?php
$updator = new RRDUpdater("speed.rrd");
//updates the data source "speed" with value "12411"
//for time defined by timestamp "920807700"
$updator->update(array("speed" => "12411"), "920807700");
?>
```
