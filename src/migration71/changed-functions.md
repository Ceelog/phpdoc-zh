变动的函数
----------

### PHP 核心

-   <span class="simpara"> <span class="function">getopt</span>
    函数增加了第三个参数，这是一个可选参数。 通过以引用的方式传入参数，
    它可以用来存储参数列表中下一个参数的下标位置。 </span>
-   <span class="simpara"> <span class="function">getenv</span>
    可以不传入任何参数。 如果不传入参数，此函数会以关联数组的形式
    返回所有的环境变量。 </span>
-   <span class="simpara"> <span class="function">get\_headers</span>
    增加了一个参数， 可以用来解析自定义的流上下文。 </span>
-   <span class="simpara"> <span
    class="function">output\_reset\_rewrite\_vars</span>
    函数不再重置会话 URL 重写变量了。 </span>
-   <span class="simpara"> <span class="function">parse\_url</span>
    更加严格的限制， 并且提供对 RFC3986 的支持。 </span>
-   <span class="simpara"> <span class="function">unpack</span>
    函数增加第三个参数， 这是一个可选参数，用来指定开始解包的位置。
    </span>

### 文件系统

-   <span class="simpara"> <span
    class="function">file\_get\_contents</span> 接受负数作为搜索偏移量，
    前提是流上下文必须是可搜索的。 </span>
-   <span class="simpara"> <span class="function">tempnam</span>
    会在退回使用系统临时目录的时候，产生警告。 </span>

### JSON

-   <span class="simpara"> <span class="function">json\_encode</span>
    增加新的选项： **`JSON_UNESCAPED_LINE_TERMINATORS`**。
    这个选项可以在指定 **`JSON_UNESCAPED_UNICODE`** 选项的时候， 对于
    U+2028 和 U+2029 这两个字符不再进行转义。 </span>

### 多子节字符

-   <span class="simpara"> <span class="function">mb\_ereg</span>
    不接受无效的字节序列。 </span>
-   <span class="simpara"> <span
    class="function">mb\_ereg\_replace</span> 不接受无效的字节序列。
    </span>

### PDO

-   <span class="simpara"> <span
    class="methodname">PDO::lastInsertId</span> 在用于 PostgreSQL
    数据库的时候， 如果当前会话（到 PostgreSQL
    的数据库连接）上尚未调用过 *nextval*， 那么此方法会触发一个错误。
    </span>

### PostgreSQL

-   <span class="simpara"> <span
    class="function">pg\_last\_notice</span>
    增加一个用来指定操作的可选参数。 可使用以下常量作为此参数的值：
    **`PGSQL_NOTICE_LAST`**, **`PGSQL_NOTICE_ALL`** 或
    **`PGSQL_NOTICE_CLEAR`**。 </span>
-   <span class="simpara"> <span class="function">pg\_fetch\_all</span>
    增加第二个参数，这是一个可选参数， 它用来指定返回结果的类型 （类似于
    <span class="function">pg\_fetch\_array</span> 的第三个参数）。
    </span>
-   <span class="simpara"> <span class="function">pg\_select</span>
    增加第四个参数，这是一个可选参数， 它用来指定返回结果的类型 （类似于
    <span class="function">pg\_fetch\_array</span> 的第三个参数）。
    </span>

### Session

-   <span class="simpara"> <span class="function">session\_start</span>
    当无法成功初始化会话的时候，返回 **`FALSE`**，
    并且不会初始化超级变量 `$_SESSION`。 </span>
