其他变化
--------

-   <span class="simpara"> 在
    <a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
    配置指令中，**`E_ALL`** 现在包括了 **`E_STRICT`** 级别的错误。
    </span>
-   <span class="simpara">
    <a href="/book/snmp.html" class="link">SNMP</a> 现在有了 OOP API 。
    </span> <span class="simpara"> 现在包括 SNMP-related
    在内，函数在每个错误状态都返回 **`FALSE`** （没有这样的实例、MIB
    结束等等）。因此，特别是，当发生 SNMP-related 错误时，get/walk
    函数中断上一个行为返回一个空字符串。 </span> <span class="simpara">
    现在支持多 OID get/getnext/set 查询。 </span> <span class="simpara">
    删除 UCD-SNMP 兼容代码，考虑升级到 net-snmp v5.3+，对于 Windows
    版本需要Net-SNMP v5.4+。 </span> <span class="simpara">
    现在通过扩展来支持远程 SNMP 代理 （对等）的 IPv6 DNS
    域名解析，而不再是通过 Net-SNMP 库。 </span>
-   <span class="simpara">
    <a href="/book/openssl.html" class="link">OpenSSL</a> 现在支持 AES
    。 </span>
-   <span class="simpara"> 当使用 readline 交互模式时，
    <a href="/features/commandline.html" class="link">CLI SAPI</a>
    不再在发生致命错误时终止。 </span>
-   <span class="simpara"> 新增微秒级精度的
    <a href="/language/variables/superglobals.html" class="link">$_SERVER['REQUEST_TIME_FLOAT']</a>
    。 </span>
-   <span class="simpara"> 增加新的哈希算法： fnv132、 fnv164及 joaat
    </span>
-   <span class="simpara"> 链式字符串偏移量，例如 $a\[0\]\[0\] 中 $a
    是一个字符串， 现在能正常运行。 </span>
-   <span class="simpara"> <span class="type">SimpleXMLElement</span>
    组织成的数组现在*总是*包含所有节点，而不仅仅是第一个匹配的节点。当使用
    <span class="function">var\_dump</span> 、 <span
    class="function">var\_export</span> 以及 <span
    class="function">print\_r</span> 时，所有 <span
    class="type">SimpleXMLElement</span> 子元素*总是*被打印出来。
    </span>
-   <span class="simpara"> 现在可以在基类的抽象构造函数中强制类的
    <a href="/language/oop5/decon.html" class="link">__construct</a>
    参数。 </span>
