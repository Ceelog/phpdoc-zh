向后不兼容
----------

虽然大部分 PHP 5 的代码无需修改即可正常运行，
但是有部分代码是无法向后兼容的：

### 使用数组标识符为类定义数组类型的属性时，数组的键不会被覆盖

在 PHP 5.6 之前的版本中，为类定义数组类型的属性时，
如果数组中同时使用了显式数组键和隐式数组键，并且显式的键和隐式的序列键相同，
那么数组的键将被覆盖。例如：

``` php
<?php
class C {
    const ONE = 1;
    public $array = [
        self::ONE => 'foo',
        'bar',
        'quux',
    ];
}

var_dump((new C)->array);
?>
```

以上例程在 PHP 5.5 中的输出：

    array(2) {
      [0]=>
      string(3) "bar"
      [1]=>
      string(4) "quux"
    }

以上例程在 PHP 5.6 中的输出：

    array(3) {
      [1]=>
      string(3) "foo"
      [2]=>
      string(3) "bar"
      [3]=>
      string(4) "quux"
    }

### 严格的 <span class="function">json\_decode</span>

对于 JSON 字面量 *true*，*false* 和 *null*，如果不采用小写格式，将会被
<span class="function">json\_decode</span> 函数拒绝， 同时相应的设置
<span class="function">json\_last\_error</span>。 在之前的版本中，<span
class="function">json\_decode</span> 函数可以接受这些字面量的
全部大写或者大小写混写的格式。

此变更仅会影响传入到 <span class="function">json\_decode</span> 中的
JSON 格式无效的情况， 有效的 JSON 输入不会受到影响并且能够正确解析。

### 当使用 SSL/TLS 的时候，流封装器默认验证端点证书和主机名

All encrypted client streams now enable peer verification by default. By
default, this will use OpenSSL's default CA bundle to verify the peer
certificate. In most cases, no changes will need to be made to
communicate with servers with valid SSL certificates, as distributors
generally configure OpenSSL to use known good CA bundles.

The default CA bundle may be overridden on a global basis by setting
either the openssl.cafile or openssl.capath configuration setting, or on
a per request basis by using the
<a href="/context/ssl.html#context.ssl.cafile" class="link"><code class="parameter">cafile</code></a>
or
<a href="/context/ssl.html#context.ssl.capath" class="link"><code class="parameter">capath</code></a>
context options.

While not recommended in general, it is possible to disable peer
certificate verification for a request by setting the
<a href="/context/ssl.html#context.ssl.verify-peer" class="link"><code class="parameter">verify_peer</code></a>
context option to **`FALSE`**, and to disable peer name validation by
setting the
<a href="/context/ssl.html#context.ssl.verify-peer-name" class="link"><code class="parameter">verify_peer_name</code></a>
context option to **`FALSE`**.

### <a href="/book/gmp.html" class="link">GMP</a> 资源现为对象

<a href="/book/gmp.html" class="link">GMP</a> 资源现为对象。 GMP
扩展中的基于函数的 API 实现不受影响， 只有在代码中使用 <span
class="function">is\_resource</span> 或类似函数
来显示检测是否资源类型的代码才会受到影响。

### <a href="/book/mcrypt.html" class="link">Mcrypt</a> 函数需要有效长度的密钥和初始向量

<span class="function">mcrypt\_encrypt</span>，<span
class="function">mcrypt\_decrypt</span>， <span
class="function">mcrypt\_cbc</span>，<span
class="function">mcrypt\_cfb</span>， <span
class="function">mcrypt\_ecb</span>，<span
class="function">mcrypt\_generic</span> 以及 <span
class="function">mcrypt\_ofb</span>
函数不再接受无效长度的密钥和初始向量，
对于需要初始向量的分组加密模式，如果不提供初始向量，函数调用将会失败。

### <a href="/book/curl.html" class="link">cURL</a> 文件上传

必须先设置 CURLOPT\_SAFE\_UPLOAD 为 **`FALSE`** 才能够使用 @file
语法来上传文件。 建议使用 <span class="classname">CURLFile</span>
类来上传文件。
