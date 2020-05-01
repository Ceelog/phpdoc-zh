范例
====

**示例 \#1 基本使用范例**

``` php
<?php

$s = new SphinxClient;
$s->setServer("localhost", 6712);
$s->setMatchMode(SPH_MATCH_ANY);
$s->setMaxQueryTime(3);

$result = $s->query("test");

var_dump($result);

?>
```

以上例程的输出类似于：

    array(10) {
      ["error"]=>
      string(0) ""
      ["warning"]=>
      string(0) ""
      ["status"]=>
      int(0)
      ["fields"]=>
      array(3) {
        [0]=>
        string(7) "subject"
        [1]=>
        string(4) "body"
        [2]=>
        string(6) "author"
      }
      ["attrs"]=>
      array(0) {
      }
      ["matches"]=>
      array(1) {
        [3]=>
        array(2) {
          ["weight"]=>
          int(1)
          ["attrs"]=>
          array(0) {
          }
        }
      }
      ["total"]=>
      int(1)
      ["total_found"]=>
      int(1)
      ["time"]=>
      float(0)
      ["words"]=>
      array(1) {
        ["to"]=>
        array(2) {
          ["docs"]=>
          int(1)
          ["hits"]=>
          int(1)
        }
      }
    }
