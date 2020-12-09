新函数
------

PHP 5.3 引入了一些新函数:

PHP 核心:

-   <span class="simpara"> <span
    class="function">array\_replace</span> -
    将一个数组的元素用另外一个数组的元素进行替换. </span>
-   <span class="simpara"> <span
    class="function">array\_replace\_recursive</span> -
    将一个数组的元素用一组传递进来的数组进行递归替换. </span>
-   <span class="simpara"> <span class="function">class\_alias</span> -
    为用户定义的类创建一个别名. </span>
-   <span class="simpara"> <span
    class="function">forward\_static\_call</span> -
    从一个方法环境调用一个用户函数. </span>
-   <span class="simpara"> <span
    class="function">forward\_static\_call\_array</span> -
    从一个方法环境调用一个用户函数，使用数组中的元素作为参数. </span>
-   <span class="simpara"> <span
    class="function">gc\_collect\_cycles</span> -
    强制收集任何存在的废物循环. </span>
-   <span class="simpara"> <span class="function">gc\_disable</span> -
    撤销循环引用收集器. </span>
-   <span class="simpara"> <span class="function">gc\_enable</span> -
    激活循环引用收集器. </span>
-   <span class="simpara"> <span class="function">gc\_enabled</span> -
    返回循环引用收集器的状态. </span>
-   <span class="simpara"> <span
    class="function">get\_called\_class</span> -
    返回调用的静态方法所在的类的名称. </span>
-   <span class="simpara"> <span class="function">gethostname</span> -
    返回本地机器的当前主机名. </span>
-   <span class="simpara"> <span
    class="function">header\_remove</span> - 在使用 <span
    class="function">header</span> 函数之前移除 HTTP Header. </span>
-   <span class="simpara"> <span class="function">lcfirst</span> -
    蒋某一字符串第一个字符转化为小写. </span>
-   <span class="simpara"> <span
    class="function">parse\_ini\_string</span> - 解析配置字符串. </span>
-   <span class="simpara"> <span
    class="function">quoted\_printable\_encode</span> - 转换 8
    位的字符串为引用的可打印字符串. </span>
-   <span class="simpara"> <span class="function">str\_getcsv</span> -
    将 CSV 字符串解析为数组. </span>
-   <span class="simpara"> <span
    class="function">stream\_context\_set\_default</span> -
    设置默认的流环境. </span>
-   <span class="simpara"> <span
    class="function">stream\_supports\_lock</span> -
    如果流支持锁定则返回 **`true`**. </span>
-   <span class="simpara"> <span
    class="function">stream\_context\_get\_params</span> -
    获取一个流环境的参数. </span>
-   <span class="simpara"> <span
    class="function">streamWrapper::stream\_cast</span> -
    获取底层的流资源. </span>
-   <span class="simpara"> <span
    class="function">streamWrapper::stream\_set\_option</span> -
    更改流选项 </span>

<a href="/book/datetime.html" class="link">Date/Time</a>:

-   <span class="simpara"> <span class="function">date\_add</span> - 向
    <span class="classname">DateTime</span>
    对象增加一定数量的天，月，年，小时，分钟和秒数. </span>
-   <span class="simpara"> <span
    class="function">date\_create\_from\_format</span> -
    根据给定的格式，返回一个 <span class="classname">DateTime</span>
    对象. </span>
-   <span class="simpara"> <span class="function">date\_diff</span> -
    返回两个 <span class="classname">DateTime</span> 对象的不同之处.
    </span>
-   <span class="simpara"> <span
    class="function">date\_get\_last\_errors</span> -
    返回最后的日期/时间操作中产生的警告和错误。 </span>
-   <span class="simpara"> <span
    class="function">date\_parse\_from\_format</span> -
    获取一个日期的信息. </span>
-   <span class="simpara"> <span class="function">date\_sub</span> - 从
    <span class="classname">DateTime</span>
    对象减去一定数量的天，月，年，时和秒数. </span>
-   <span class="simpara"> <span
    class="function">timezone\_version\_get</span> -
    返回时区数据库的版本. </span>

<a href="/book/gmp.html" class="link">GMP</a>:

-   <span class="simpara"> <span class="function">gmp\_testbit</span> -
    测试一个比特是否被设置. </span>

<a href="/book/hash.html" class="link">Hash</a>:

-   <span class="simpara"> <span class="function">hash\_copy</span> -
    复制哈希环境. </span>

<a href="/book/imap.html" class="link">IMAP</a>:

-   <span class="simpara"> <span class="function">imap\_gc</span> - 清除
    IMAP 缓存. </span>
-   <span class="simpara"> <span
    class="function">imap\_utf8\_to\_mutf7</span> - 编码 UTF-8
    字符串为改进的 UTF-7 编码. </span>
-   <span class="simpara"> <span
    class="function">imap\_mutf7\_to\_utf8</span> - 解码改进的 UTF-7
    字符串为 UTF-8 编码. </span>

<a href="/book/json.html" class="link">JSON</a>:

-   <span class="simpara"> <span
    class="function">json\_last\_error</span> - 返回最后发生的 JSON
    错误。 </span>

<a href="/set/mysqlinfo.html#Mysqli" class="link">MySQL 改进</a>:

-   <span class="simpara"> <span
    class="function">mysqli\_fetch\_all</span> -
    以关联数组、索引数组或者二者都有获取全部结果行. </span>
-   <span class="simpara"> <span
    class="function">mysqli\_get\_connection\_stats</span> -
    返回客户端连接的统计资料. </span>
-   <span class="simpara"> <span class="function">mysqli\_poll</span> -
    轮询连接. </span>
-   <span class="simpara"> <span
    class="function">mysqli\_reap\_async\_query</span> -
    从异步查询中获取结果. </span>

<a href="/book/openssl.html" class="link">OpenSSL</a>:

-   <span class="simpara"> <span
    class="function">openssl\_random\_pseudo\_bytes</span> -
    返回一个以伪随机字节填充的指定长度的字符串. </span>

<a href="/book/pcntl.html" class="link">PCNTL</a>:

-   <span class="simpara"> <span
    class="function">pcntl\_signal\_dispatch</span> -
    为挂起信号调用信号处理器. </span>
-   <span class="simpara"> <span
    class="function">pcntl\_sigprocmask</span> - 设置和获取阻塞信号.
    </span>
-   <span class="simpara"> <span
    class="function">pcntl\_sigtimedwait</span> -
    等待信号，但是有超时时间. </span>
-   <span class="simpara"> <span
    class="function">pcntl\_sigwaitinfo</span> - 等待信号. </span>

<a href="/book/pcre.html" class="link">PCRE</a>:

-   <span class="simpara"> <span class="function">preg\_filter</span> -
    执行正则查找和替换，仅仅返回匹配正则的结果. </span>

<a href="/book/sem.html" class="link">信号</a>:

-   <span class="simpara"> <span
    class="function">msg\_queue\_exists</span> - 检查消息队列是否存在.
    </span>
-   <span class="simpara"> <span class="function">shm\_has\_var</span> -
    检查在一个共享内存段中，是否存在指定的键(key). </span>

以下函数被原生支持，因此它们在所有运行 PHP 的操作系统上均可用。

-   <span class="simpara"> <span class="function">acosh</span> </span>
-   <span class="simpara"> <span class="function">asinh</span> </span>
-   <span class="simpara"> <span class="function">atanh</span> </span>
-   <span class="simpara"> <span class="function">expm1</span> </span>
-   <span class="simpara"> <span class="function">log1p</span> </span>
