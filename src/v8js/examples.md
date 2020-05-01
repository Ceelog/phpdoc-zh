范例
====

Basic usage

**示例 \#1 Basic Javascript execution**

``` php
<?php

$v8 = new V8Js();

/* basic.js */
$JS = <<< EOT
len = print('Hello' + ' ' + 'World!' + "\\n");
len;
EOT;

try {
  var_dump($v8->executeString($JS, 'basic.js'));
} catch (V8JsException $e) {
  var_dump($e);
}

?>
```

以上例程会输出：

    Hello World!
    int(13)
