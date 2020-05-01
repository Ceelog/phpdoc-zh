Reading \[\]
------------

``` php
<?php
class XmlTest {

    function test_ref(&$test) {
        $test = "ok";
    }

    function test($test) { }

    function run() {
        $ar = array();
        $this->test_ref($ar[]);
        var_dump($ar);
        $this->test($ar[]);
    }
}

$o = new XmlTest();
$o->run();
?>
```

This should always have thrown a fatal **`E_ERROR`**, because \[\]
cannot be used for reading in PHP. It is invalid code in PHP 4.4.2 and
PHP 5.0.5 upward.
