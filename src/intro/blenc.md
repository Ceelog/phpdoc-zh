**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担。

BLENC is a PHP source script protector that:

-   Encodes your source code with the blowfish algorithm.
-   Allows transparent decryption and execution of PHP scripts
    previously encoded with BLENC.

BLENC is an extension which hooks into the Zend Engine, allowing for
transparent encryption and execution of PHP scripts using the blowfish
algorithm. It is not designed for complete security (it is still
possible to disassemble the script into op codes using a package such as
XDebug), however it does keep people out of your code and make reverse
engineering difficult.

In order to protect your PHP script you must encrypt each script with
<span class="function">blenc\_encrypt</span> function. After you can
include the encoded script like the example below:

``` php
<?php

/* PHP script encoded with BLENC */
$my_source_encoded = 'my_source_encoded.phpe';

include($my_source_encoded);
?>
```

BLENC supports also expiration time for the module. So, if you want
deploy your source code with a expiration time, you have to compile the
extension modifying the header file related to encryption and expiration
time. Please see configuration section for further informations.
