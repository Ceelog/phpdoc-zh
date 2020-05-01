函数的变化
----------

### PHP 内核

-   <span class="simpara"> 如果省略 `salt` 参数，<span
    class="function">crypt</span> 会产生 **`E_NOTICE`**错误。 </span>
-   <span class="simpara"> <span class="function">substr\_compare</span>
    的 `length` 参数现在接受 *0* 的值。 </span>
-   <span class="simpara"> <span class="function">unserialize</span>
    will now fail if passed serialised data that has been manipulated to
    attempt to instantiate an object without calling its constructor.
    </span>

### <a href="/book/curl.html" class="link">cURL</a>

-   <span class="simpara"> 只有设置 **`CURLOPT_SAFE_UPLOAD`** 为
    **`FALSE`** 的情况下， 才接受 *@file* 语法上传文件。 最好使用 <span
    class="classname">CURLFile</span> 代替。 </span>

### <a href="/book/mcrypt.html" class="link">Mcrypt</a>

-   <span class="simpara"> <span
    class="function">mcrypt\_create\_iv</span> 的 `source` 现在默认值是
    **`MCRYPT_DEV_URANDOM`**，而非 **`MCRYPT_DEV_RANDOM`**。 </span>

### <a href="/book/openssl.html" class="link">OpenSSL</a>

-   <span class="simpara"> 如果 SSL 上下文选项已经提供 `crypto_type`
    选项， <span class="function">stream\_socket\_enable\_crypto</span>
    可以忽略 `crypto_type` 参数。 </span>

### <a href="/book/pgsql.html" class="link">PostgreSQL</a>

-   <span class="simpara"> <span
    class="function">pg\_insert</span>、<span
    class="function">pg\_select</span>、 <span
    class="function">pg\_update</span>、<span
    class="function">pg\_delete</span> 不再是实验性质的。 </span>
-   <span class="simpara"> 如果数据库连接 socket
    流设置为非阻塞（non-blocking）模式， <span
    class="function">pg\_send\_execute</span>、 <span
    class="function">pg\_send\_prepare</span>、<span
    class="function">pg\_send\_query</span> 、<span
    class="function">pg\_send\_query\_params</span>
    不再会阻塞查询直到写入完成。 </span>

### <a href="/book/reflection.html" class="link">Reflection</a>

-   <span class="simpara"> <span
    class="methodname">ReflectionClass::newInstanceWithoutConstructor</span>
    现在允许非 Final 的内部类实例化。 </span>

### <a href="/book/xmlreader.html" class="link">XMLReader</a>

-   <span class="simpara"> 和 <span
    class="methodname">XMLReader::getAttribute</span>
    一样，未找到属性的情况下， <span
    class="methodname">XMLReader::getAttributeNs</span> 和 <span
    class="methodname">XMLReader::getAttributeNo</span> 会返回
    **`NULL`** 。 </span>
