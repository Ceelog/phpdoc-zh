范例
====

**目录**

-   [Basic usage](/swish/examples.html#Basic%20usage)

Basic usage
-----------

**示例 \#1 Basic search query**

``` php
<?php

try {

    $swish = new Swish("index.swish-e");
    $results = $swish->query("test OR text");

    echo "Found ", $results->hits, " results\n";
    while ($result = $results->nextResult()) {
        var_dump($result);
        break; //break after the first result
    }

} catch (SwishException $e) {
    echo "Error: ", $e->getMessage(), "\n";
}

?>
```

以上例程的输出类似于：

    Found 9 results
    object(SwishResult)#3 (8) {
      ["swishreccount"]=>
      int(1)
      ["swishrank"]=>
      int(1000)
      ["swishfilenum"]=>
      int(10)
      ["swishdbfile"]=>
      string(13) "index.swish-e"
      ["swishdocpath"]=>
      string(23) "README.SUBMITTING_PATCH"
      ["swishtitle"]=>
      NULL
      ["swishdocsize"]=>
      int(4557)
      ["swishlastmodified"]=>
      int(1072136752)
    }
