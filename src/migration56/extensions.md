扩展中的变动
------------

### <a href="/book/curl.html" class="link">cURL</a>

在 cURL 库中的一些被标记为废弃的常量， 现在已经被移除：

-   <span class="simpara"> **`CURLOPT_CLOSEPOLICY`** </span>
-   <span class="simpara"> **`CURLCLOSEPOLICY_CALLBACK`** </span>
-   <span class="simpara"> **`CURLCLOSEPOLICY_LEAST_RECENTLY_USED`**
    </span>
-   <span class="simpara"> **`CURLCLOSEPOLICY_LEAST_TRAFFIC`** </span>
-   <span class="simpara"> **`CURLCLOSEPOLICY_OLDEST`** </span>
-   <span class="simpara"> **`CURLCLOSEPOLICY_SLOWEST`** </span>

### <a href="/book/oci8.html" class="link">OCI8</a>

-   <span class="simpara"> 加入 <span
    class="function">oci\_get\_implicit\_resultset</span> 函数 来支持
    Oracle Database 12c 的隐式结果集。 </span>
-   <span class="simpara"> 如果使用 *oci\_execute($s,
    OCI\_NO\_AUTO\_COMMIT)* 执行 SELECT 语句，
    在连接关闭时发起内部的事物回滚不再是冗余的。 </span>
-   <span class="simpara"> 通过 *--enable-dtrace* 配置选项 控制 DTrace
    探针。 </span>
-   <span class="simpara"> <span
    class="function">oci\_internal\_debug</span> 现在是无操作函数。
    </span>
-   <span class="simpara"> 在 <span class="function">phpinfo</span>
    输出中 OCI8 的格式发生变动。 </span>

### <a href="/book/zip.html" class="link">Zip</a>

加入 *--with-libzip* 配置选项， 使得你可以使用系统安装的 libzip。
最低支持 libzip 0.11 版本，建议使用 0.11.2 或更高的版本。

### <a href="/set/mysqlinfo.html#Mysqli" class="link">MySQLi</a>

新加
<a href="/set/mysqlinfo.html#" class="link">mysqli.rollback_on_cached_plink</a>
选项，对于事务回滚的连接，将其返回到持久连接池中。
