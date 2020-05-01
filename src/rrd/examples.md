范例
====

**目录**

-   [Procedural PECL/rrd
    example](/rrd/examples.html#Procedural%20PECL/rrd%20example)
-   [OOP PECL/rrd example](/rrd/examples.html#OOP%20PECL/rrd%20example)

Procedural PECL/rrd example
---------------------------

**示例 \#1 Procedural usage of rrd**

``` php
<?php
$rrdFile = dirname(__FILE__) . "/speed.rrd";

//create rrd file
rrd_create($rrdFile,
 array(
  "--start",920804400,
  "DS:speed:COUNTER:600:U:U",
  "RRA:AVERAGE:0.5:1:24",
  "RRA:AVERAGE:0.5:6:10"
  )
);

//update rrd file
rrd_update($rrdFile,
 array(
  "920804700:12345",
  "920805000:12357"
  )
);

//graph output
rrd_graph(dirname(__FILE__) . "/speed.png",
 array(
  "--start", "920804400",
  "--end", "920808000",
  "--vertical-label", "m/s",
  "DEF:myspeed=$rrdFile:speed:AVERAGE",
  "CDEF:realspeed=myspeed,1000,*",
  "LINE2:realspeed#FF0000"
 )
);
?>
```

OOP PECL/rrd example
--------------------

**示例 \#1 OO usage of rrd**

``` php
<?php
$rrdFile = dirname(__FILE__) . "/speed.rrd";
$outputPngFile = dirname(__FILE__) . "/speed.png";

$creator = new RRDCreator($rrdFile, "now -10d", 500);
$creator->addDataSource("speed:COUNTER:600:U:U");
$creator->addArchive("AVERAGE:0.5:1:24");
$creator->addArchive("AVERAGE:0.5:6:10");
$creator->save();

$updater = new RRDUpdater($rrdFile);
$updater->update(array("speed" => "12345"), "920804700");
$updater->update(array("speed" => "12357"), "920805000");

$graphObj = new RRDGraph($outputPngFile);
$graphObj->setOptions(
    array(
        "--start" => "920804400",
        "--end" => 920808000,
        "--vertical-label" => "m/s",
        "DEF:myspeed=$rrdFile:speed:AVERAGE",
        "CDEF:realspeed=myspeed,1000,*",
        "LINE2:realspeed#FF0000"
    )
);
$graphObj->save();
?>
```
