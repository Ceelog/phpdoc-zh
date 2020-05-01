Other changes to extensions
---------------------------

以下扩展不再能在编译配置时进行关闭:

-   <span class="simpara">
    <a href="/book/pcre.html" class="link">PCRE</a> </span>
-   <span class="simpara">
    <a href="/book/reflection.html" class="link">反射</a> </span>
-   <span class="simpara"> <a href="/book/spl.html" class="link">SPL</a>
    </span>

扩展行为和新功能的改变:

-   <span class="simpara">
    <a href="/book/datetime.html" class="link">日期和时间</a> -
    获取时区时不再使用 TZ 环境变量. </span>
-   <span class="simpara">
    <a href="/book/curl.html" class="link">cURL</a> - cURL 支持 SSH
    </span>
-   <span class="simpara">
    <a href="/book/network.html" class="link">Network</a> - <span
    class="function">dns\_check\_record</span> 现在返回一个额外的
    "entries" 索引, 包含 TXT 元素. </span>
-   <span class="simpara">
    <a href="/book/hash.html" class="link">Hash</a> - SHA-224 和 salsa
    哈希算法获得支持. </span>
-   <span class="simpara">
    <a href="/book/mbstring.html" class="link">mbstring</a> - 现在支持
    CP850 编码. </span>
-   <span class="simpara">
    <a href="/book/oci8.html" class="link">OCI8</a> - 在持久连接上调用
    <span class="function">oci\_close</span> 或者在作用域外引用持久连接,
    将回滚任何尚未提交的事务. 为了避免意外的行为,
    根据需要明确发布和回滚事务. 使用 INI
    指令<a href="/book/oci8.html#" class="link">oci8.old_oci_close_semantics</a>可以打开旧的行为.
    </span> <span class="simpara">
    数据库驻留连接池(DRCP)和快速应用通知(FAN)获得支持. </span> <span
    class="simpara"> Oracle 外部认证获得支持(除了 Windows 平台). </span>
    <span class="simpara"> <span
    class="function">oci\_bind\_by\_name</span> 函数现在支持 SQLT\_AFC
    (又称 CHAR 数据类型). </span>
-   <span class="simpara">
    <a href="/book/openssl.html" class="link">OpenSSL</a> - 支持 OpenSSL
    摘要和加密函数. 访问 DSA, RSA 和 DH 键的内部值变为可能. </span>
-   <span class="simpara">
    <a href="/book/session.html" class="link">Session</a> - 当应用了
    <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
    限制, Session 不再将 Session 文件存储在 *"/tmp"* 目录中, 除非
    *"/tmp"* 目录被明确添加到许可路径列表. </span>
-   <span class="simpara">
    <a href="/book/soap.html" class="link">SOAP</a> 支持发送用户提供的
    HTTP 头. </span>
-   <span class="simpara">
    <a href="/set/mysqlinfo.html#Mysqli" class="link">MySQLi</a>
    通过在主机名前面添加 *"p:"* 来支持持久连接. </span>
-   <span class="simpara">
    <a href="/book/image.html" class="link">图片处理和 GD</a> <span
    class="function">gd\_info</span> 函数返回的 "JPG Support" 索引变更为
    "JPEG Support". </span>
