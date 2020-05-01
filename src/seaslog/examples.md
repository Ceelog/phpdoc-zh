范例
====

**示例 \#1 获取与设置根目录**

``` php
<?php
  $basePath1 = SeasLog::getBasePath();

  SeasLog::setBasePath('/log/base_test');
  $basePath2 = SeasLog::getBasePath();

  var_dump($basePath1,$basePath2);

  ?>
```

以上例程的输出类似于：

      string(12) "/var/log/www"
      string(14) "/log/base_test"
      

**示例 \#2 获取与设置 Logger**

``` php
<?php
$lastLogger1 = SeasLog::getLastLogger();

SeasLog::setLogger('testModule/app1');
$lastLogger2 = SeasLog::getLastLogger();

var_dump($lastLogger1,$lastLogger2);

?>
```

以上例程的输出类似于：

    string(7) "default"
    string(15) "testModule/app1"

**示例 \#3 快速写入日志**

``` php
<?php
SeasLog::log(SEASLOG_ERROR,'this is a error test by ::log');
SeasLog::debug('this is a {userName} debug',array('{userName}' => 'neeke'));
SeasLog::info('this is a info log');
SeasLog::notice('this is a notice log');
SeasLog::warning('your {website} was down,please {action} it ASAP!',array('{website}' => 'github.com','{action}' => 'rboot'));
SeasLog::error('a error log');
SeasLog::critical('some thing was critical');
SeasLog::alert('yes this is a {messageName}',array('{messageName}' => 'alertMSG'));
SeasLog::emergency('Just now, the house next door was completely burnt out! {note}',array('{note}' => 'it`s a joke'));
?>
```

日志的默认模板是 *seaslog.default\_template = "%T \| %L \| %P \| %Q \|
%t \| %M"*. 这意味着，在默认情况下，日志的记录格式是： \`{dateTime} \|
{level} \| {pid} \| {uniqid} \| {timeStamp} \| {logInfo}\`.

以上例程的输出类似于：

*seaslog.appender = 1*

    2014-07-27 08:53:52 | ERROR | 23625 | 599159975a9ff | 1406422432.786 | this is a error test by log
    2014-07-27 08:53:52 | DEBUG | 23625 | 599159975a9ff | 1406422432.786 | this is a neeke debug
    2014-07-27 08:53:52 | INFO | 23625 | 599159975a9ff | 1406422432.787 | this is a info log
    2014-07-27 08:53:52 | NOTICE | 23625 | 599159975a9ff | 1406422432.787 | this is a notice log
    2014-07-27 08:53:52 | WARNING | 23625 | 599159975a9ff | 1406422432.787 | your github.com was down,please rboot it ASAP!
    2014-07-27 08:53:52 | ERROR | 23625 | 599159975a9ff | 1406422432.787 | a error log
    2014-07-27 08:53:52 | CRITICAL | 23625 | 599159975a9ff | 1406422432.787 | some thing was critical
    2014-07-27 08:53:52 | EMERGENCY | 23625 | 599159975a9ff | 1406422432.787 | Just now, the house next door was completely burnt out! it is a joke

以上例程的输出类似于：

*seaslog.appender = 2* or *seaslog.appender = 3*

    The log style finally formatted such as:
    <15>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | DEBUG | 21423 | 599157af4e937 | 1466787583.322 | this is a neeke debug
    <14>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | INFO | 21423 | 599157af4e937 | 1466787583.323 | this is a info log
    <13>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | NOTICE | 21423 | 599157af4e937 | 1466787583.324 | this is a notice log

**示例 \#4 快速获取某级别下日志的数量**

*SeasLog* 通过系统命令管道调用 \`grep -wc\` 获取数量，并返回给 PHP
(返回数组或单个数值).

``` php
<?php
$countResult1 = SeasLog::analyzerCount();
$countResult2 = SeasLog::analyzerCount(SEASLOG_WARNING);
$countResult3 = SeasLog::analyzerCount(SEASLOG_ERROR,date('Ymd',time()));

var_dump($countResult1,$countResult2,$countResult3);

?>
```

以上例程的输出类似于：

    array(8) {
      ["DEBUG"]=>
      int(3)
      ["INFO"]=>
      int(3)
      ["NOTICE"]=>
      int(3)
      ["WARNING"]=>
      int(3)
      ["ERROR"]=>
      int(6)
      ["CRITICAL"]=>
      int(3)
      ["ALERT"]=>
      int(3)
      ["EMERGENCY"]=>
      int(3)
    }
    int(7)
    int(1)

**示例 \#5 获取某级别下日志的详情**

*SeasLog* 通过系统命令管道调用 \`grep -w\` 获取日志详情，并返回数组给
PHP.

``` php
<?php
$detailErrorArray = SeasLog::analyzerDetail(SEASLOG_ERROR);
var_dump($detailErrorArray);

var_dump(SeasLog::analyzerDetail(SEASLOG_ERROR,date('Ymd',time())));
?>
```

以上例程的输出类似于：

    array(6) {
      [0] =>
      string(83) "2014-02-24 00:14:02 | ERROR | 8568 | 599157af4e937 | 1393172042.717 | test error 3 "
      [1] =>
      string(83) "2014-02-24 00:14:04 | ERROR | 8594 | 5991576584446 | 1393172044.104 | test error 3 "
      [2] =>
      string(83) "2014-02-24 00:14:04 | ERROR | 8620 | 1502697015147 | 1393172044.862 | test error 3 "
      [3] =>
      string(83) "2014-02-24 00:14:05 | ERROR | 8646 | 599159975a9ff | 1393172045.989 | test error 3 "
      [4] =>
      string(83) "2014-02-24 00:14:07 | ERROR | 8672 | 599159986ec28 | 1393172047.882 | test error 3 "
      [5] =>
      string(83) "2014-02-24 00:14:08 | ERROR | 8698 | 5991599981cec | 1393172048.736 | test error 3 "
    }

    array(2) {
      [0] =>
      string(83) "2014-02-24 00:14:02 | ERROR | 8568 | 599157af4e937 | 1393172042.717 | test error 3 "
      [1] =>
      string(83) "2014-02-24 00:14:04 | ERROR | 8594 | 5991576584446 | 1393172044.104 | test error 3 "
    }
