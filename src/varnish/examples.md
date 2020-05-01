范例
====

**目录**

-   [Basic VarnishAdmin
    usage](/varnish/examples.html#Basic%20VarnishAdmin%20usage)
-   [Basic VarnishStat
    usage](/varnish/examples.html#Basic%20VarnishStat%20usage)
-   [Basic VarnishLog
    usage](/varnish/examples.html#Basic%20VarnishLog%20usage)

Basic VarnishAdmin usage
------------------------

The example illustrates a simple usage of the ban functionality

**示例 \#1 Ban an URL**

``` php
<?php

$args = array(
    VARNISH_CONFIG_HOST    => "::1",
    VARNISH_CONFIG_PORT    => 6082,
    VARNISH_CONFIG_SECRET  => "5174826b-8595-4958-aa7a-0609632ad7ca",
    VARNISH_CONFIG_TIMEOUT => 300,
);

$va = new VarnishAdmin($args);

try {
    if(!$va->connect()) {
        throw new VarnishException("Connection failed\n");
    }   
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

try {
    if(!$va->auth()) {
        throw new VarnishException("Auth failed\n");
    }   
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

try {
    $status = $va->ban('req.url ~ "^/$"');
    if (VARNISH_STATUS_OK != $status) {
        throw new VarnishException("Ban method returned $status status\n");
    }
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

exit(0);

?>
```

Basic VarnishStat usage
-----------------------

The example illustrates getting varnish statistic snapshot from shared
memory

**示例 \#1 Get statistic snapshot**

``` php
<?php

$vs = new VarnishStat;

try {
    $data = $vs->getSnapshot();
} catch (VarnishException $e) {
    echo $e->getMessage();
    exit(3);
}

exit(0);
?>
```

Basic VarnishLog usage
----------------------

The example illustrates reading varnish log lines from shared memory

**示例 \#1 Read varnish shared memory log**

``` php
<?php

$vl = new VarnishLog;
while(1) {
    $line = $vl->getLine();
    printf("%s %d %s", VarnishLog::getTagName($line['tag'], $line['id'],
    $line['data']);
}

exit(0);
?>
```
