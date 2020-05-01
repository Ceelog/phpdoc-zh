加密过滤器
----------

*mcrypt.\**和 *mdecrypt.\**使用 libmcrypt
提供了对称的加密和解密。这两组过滤器都支持
<a href="/ref/mcrypt.html" class="link">mcrypt 扩展库</a>中相同的算法，格式为
*mcrypt.ciphername*，其中 `ciphername`是密码的名字，将被传递给 <span
class="function">mcrypt\_module\_open</span>。有以下五个过滤器参数可用：

| 参数            | 是否必须 | 默认值                             | 取值举例                                          |
|-----------------|----------|------------------------------------|---------------------------------------------------|
| mode            | 可选     | cbc                                | cbc, cfb, ecb, nofb, ofb, stream                  |
| algorithms\_dir | 可选     | ini\_get('mcrypt.algorithms\_dir') | algorithms 模块的目录                             |
| modes\_dir      | 可选     | ini\_get('mcrypt.modes\_dir')      | modes 模块的目录                                  |
| iv              | 必须     | N/A                                | 典型为 8，16 或 32 字节的二进制数据。根据密码而定 |
| key             | 必须     | N/A                                | 典型为 8，16 或 32 字节的二进制数据。根据密码而定 |

**示例 \#1 用 3DES 将文件加密输出**

``` php
<?php
$passphrase = 'My secret';

/* Turn a human readable passphrase
 * into a reproducable iv/key pair
 */
$iv = substr(md5('iv'.$passphrase, true), 0, 8);
$key = substr(md5('pass1'.$passphrase, true) .
               md5('pass2'.$passphrase, true), 0, 24);
$opts = array('iv'=>$iv, 'key'=>$key);

$fp = fopen('secert-file.enc', 'wb');
stream_filter_append($fp, 'mcrypt.tripledes', STREAM_FILTER_WRITE, $opts);
fwrite($fp, 'Secret secret secret data');
fclose($fp);
?>
```

**示例 \#2 读取加密的文件**

``` php
<?php
$passphrase = 'My secret';

/* Turn a human readable passphrase
 * into a reproducable iv/key pair
 */
$iv = substr(md5('iv'.$passphrase, true), 0, 8);
$key = substr(md5('pass1'.$passphrase, true) .
               md5('pass2'.$passphrase, true), 0, 24);
$opts = array('iv'=>$iv, 'key'=>$key);

$fp = fopen('secert-file.enc', 'rb');
stream_filter_append($fp, 'mdecrypt.tripledes', STREAM_FILTER_WRITE, $opts);
$data = rtrim(stream_get_contents($fp));
fclose($fp);

echo $data;
?>
```
