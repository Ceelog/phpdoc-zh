新函数
------

PHP 5 有了些新函数。下面是列表：

<a href="/ref/array.html" class="link">Arrays</a>:

-   <span class="simpara"> <span class="function">array\_combine</span>
    - 用一个数组作为键名，另一个数组作为值创建一个新数组 </span>
-   <span class="simpara"> <span
    class="function">array\_diff\_uassoc</span> -
    计算数组的差别，并用用户提供的回调函数作附加的索引检查 </span>
-   <span class="simpara"> <span class="function">array\_udiff</span> -
    用回调函数比较数据来计算数组的差别 </span>
-   <span class="simpara"> <span
    class="function">array\_udiff\_assoc</span> -
    计算数组的差别并作附加的索引检查。用回调函数来比较数据 </span>
-   <span class="simpara"> <span
    class="function">array\_udiff\_uassoc</span> -
    计算数组的差别并作附加的索引检查。数据的比较和索引检查都用回调函数来完成
    </span>
-   <span class="simpara"> <span
    class="function">array\_walk\_recursive</span> -
    对数组的每个成员递归使用用户函数 </span>
-   <span class="simpara"> <span
    class="function">array\_uintersect\_assoc</span> -
    计算数组的交集并作附加的索引检查。用回调函数来比较数据 </span>
-   <span class="simpara"> <span
    class="function">array\_uintersect\_uassoc</span> -
    计算数组的交集并作附加的索引检查。数据和索引都用回调函数来比较
    </span>
-   <span class="simpara"> <span
    class="function">array\_uintersect</span> -
    计算数组的交集。用回调函数来比较数据 </span>

<a href="/book/ibase.html#Firebird/InterBase%20函数" class="link">InterBase</a>:

-   <span class="simpara"> <span
    class="function">ibase\_affected\_rows</span> -
    返回前一个查询影响到的行的数目 </span>
-   <span class="simpara"> <span class="function">ibase\_backup</span> -
    在服务管理器中发起一个后台任务并立即返回 </span>
-   <span class="simpara"> <span
    class="function">ibase\_commit\_ret</span> - 提交一个事务但不关闭
    </span>
-   <span class="simpara"> <span class="function">ibase\_db\_info</span>
    - 请求有关数据库的统计信息 </span>
-   <span class="simpara"> <span
    class="function">ibase\_drop\_db</span> - 删除一个数据库 </span>
-   <span class="simpara"> <span
    class="function">ibase\_errcode</span> - 返回一个错误代码 </span>
-   <span class="simpara"> <span
    class="function">ibase\_free\_event\_handler</span> -
    取消一个已注册的事件句柄 </span>
-   <span class="simpara"> <span class="function">ibase\_gen\_id</span>
    - 递增指定的发生器并返回其新值 </span>
-   <span class="simpara"> <span
    class="function">ibase\_maintain\_db</span> -
    在数据库服务器上执行一条维护命令 </span>
-   <span class="simpara"> <span
    class="function">ibase\_name\_result</span> - 给结果集指定一个名字
    </span>
-   <span class="simpara"> <span
    class="function">ibase\_num\_params</span> -
    返回一个准备好的查询的参数数目 </span>
-   <span class="simpara"> <span
    class="function">ibase\_param\_info</span> -
    返回一个准备好的查询的参数信息 </span>
-   <span class="simpara"> <span class="function">ibase\_restore</span>
    - 在服务管理器中发起一个还原任务并立即返回 </span>
-   <span class="simpara"> <span
    class="function">ibase\_rollback\_ret</span> -
    回卷一笔事务并保留事务上下文 </span>
-   <span class="simpara"> <span
    class="function">ibase\_server\_info</span> -
    请求有关数据库服务器的统计信息 </span>
-   <span class="simpara"> <span
    class="function">ibase\_service\_attach</span> - 连接到服务管理器
    </span>
-   <span class="simpara"> <span
    class="function">ibase\_service\_detach</span> - 从服务管理器断开
    </span>
-   <span class="simpara"> <span
    class="function">ibase\_set\_event\_handler</span> -
    注册一个当事件发布时要调用的回调函数 </span>
-   <span class="simpara"> <span
    class="function">ibase\_wait\_event</span> - 等待数据库发布一条事件
    </span>

<a href="/ref/iconv.html" class="link">iconv</a>:

-   <span class="simpara"> <span
    class="function">iconv\_mime\_decode</span> - 解码 MIME 头信息字段
    </span>
-   <span class="simpara"> <span
    class="function">iconv\_mime\_decode\_headers</span> - 一次解码多个
    MIME 头信息字段 </span>
-   <span class="simpara"> <span
    class="function">iconv\_mime\_encode</span> - 压缩 MIME 头信息字段
    </span>
-   <span class="simpara"> <span class="function">iconv\_strlen</span> -
    返回字符串中的字符计数 </span>
-   <span class="simpara"> <span class="function">iconv\_strpos</span> -
    在堆栈中找到第一个出现的子串位置 </span>
-   <span class="simpara"> <span class="function">iconv\_strrpos</span>
    - 在堆栈中找到最后一个出现的子串位置 </span>
-   <span class="simpara"> <span class="function">iconv\_substr</span> -
    从字符串中取出一部分 </span>

<a href="/ref/stream.html" class="link">Streams</a>:

-   <span class="simpara"> <span
    class="function">stream\_copy\_to\_stream</span> -
    把一个流的数据复制到另一个流 </span>
-   <span class="simpara"> <span
    class="function">stream\_get\_line</span> -
    根据给定的分隔符中流中读取一行 </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_accept</span> - 接受一个由 <span
    class="function">stream\_socket\_server</span> 建立的 socket 连接
    </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_client</span> - 打开一个 Internet
    或 Unix 域的 socket 连接 </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_get\_name</span> - 获取本地或远程的
    sockets 名字 </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_recvfrom</span> - 从 socket
    获取数据（不管连接是否已经建立） </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_sendto</span> - 向 socket
    发送一个消息（不管连接是否已经建立） </span>
-   <span class="simpara"> <span
    class="function">stream\_socket\_server</span> - 建立一个 Internet
    或 Unix 域服务器的 socket </span>

<a href="/ref/datetime.html" class="link">Date/Time</a>:

-   <span class="simpara"> <span class="function">idate</span> -
    将本地时间格式化为整数 </span>
-   <span class="simpara"> <span class="function">date\_sunset</span> -
    计算所指定日期和地点的日落时间 </span>
-   <span class="simpara"> <span class="function">date\_sunrise</span> -
    T计算所指定日期和地点的日出时间 </span>
-   <span class="simpara"> <span
    class="function">time\_nanosleep</span> - 廷迟执行程若干秒和若干纳秒
    </span>

<a href="/ref/strings.html" class="link">Strings</a>:

-   <span class="simpara"> <span class="function">str\_split</span> -
    把一个字符串分割为数组 </span>
-   <span class="simpara"> <span class="function">strpbrk</span> -
    在一字符串中搜索给定的字符集合中的任意一个字符 </span>
-   <span class="simpara"> <span
    class="function">substr\_compare</span> -
    以二进制的形式比较两个字符串，从第一个字符串的 offset
    开始，直到到达长度为 length 时结束，可自定义是否大小写敏感比较
    </span>

Other:

-   <span class="simpara"> <span
    class="function">convert\_uudecode</span> - 解码 uuencoded 的字符串
    </span>
-   <span class="simpara"> <span
    class="function">convert\_uuencode</span> - 对字符串进行 uuencode
    </span>
-   <span class="simpara"> <span
    class="function">curl\_copy\_handle</span> - 复制一个 cURL
    句柄及其所有参数 </span>
-   <span class="simpara"> <span
    class="function">dba\_key\_split</span> - 把一个键分隔为字符串数组
    </span>
-   <span class="simpara"> <span
    class="function">dbase\_get\_header\_info</span> - 取得 dBase
    数据库的头部信息 </span>
-   <span class="simpara"> <span
    class="function">dbx\_fetch\_row</span> - 获取结果集中被设置为
    DBX\_RESULT\_UNBUFFERED 的行 </span>
-   <span class="simpara"> <span
    class="function">fbsql\_set\_password</span> - 修改指定用户的密码
    </span>
-   <span class="simpara"> <span
    class="function">file\_put\_contents</span> - 向一个文件内写入字符串
    </span>
-   <span class="simpara"> <span class="function">ftp\_alloc</span> -
    为准备上传的文件分配空间 </span>
-   <span class="simpara"> <span
    class="function">get\_declared\_interfaces</span> -
    以数组的形式返回所有已定义的接品 </span>
-   <span class="simpara"> <span class="function">get\_headers</span> -
    获取服务器响应 HTTP 请求时的所有头部信息 </span>
-   <span class="simpara"> <span class="function">headers\_list</span> -
    返回所有已发送或准备发送响应头部列表 </span>
-   <span class="simpara"> <span
    class="function">http\_build\_query</span> - 生成一个已经过 URL
    编码的请求字符串 </span>
-   <span class="simpara"> <span
    class="function">image\_type\_to\_extension</span> - 根据 <span
    class="function">getimagesize</span>, <span
    class="function">exif\_read\_data</span>, <span
    class="function">exif\_thumbnail</span>, <span
    class="function">exif\_imagetype</span> 所返回的 image-type
    取得文件名后缀 </span>
-   <span class="simpara"> <span class="function">imagefilter</span> -
    对图像应用滤镜 </span>
-   <span class="simpara"> <span class="function">imap\_getacl</span> -
    获取指定邮箱的 ACL </span>
-   <span class="simpara"> <span
    class="function">ldap\_sasl\_bind</span> - 使用 SASL 绑定到 LDAP
    目录 </span>
-   <span class="simpara"> <span
    class="function">mb\_list\_encodings</span> -
    以数组的形式返回所支持的全部字符集 </span>
-   <span class="simpara"> <span
    class="function">pcntl\_getpriority</span> -
    获得任意一个进程的优先级 </span>
-   <span class="simpara"> <span class="function">pcntl\_wait</span> -
    Waits on or returns the status of a forked child as defined by the
    waitpid() system call </span>
-   <span class="simpara"> <span class="function">pg\_version</span> -
    返回一个包含客户端、协议和服务器版本的数组 </span>
-   <span class="simpara"> <span
    class="function">php\_check\_syntax</span> - 检查指定文件的语法
    </span>
-   <span class="simpara"> <span
    class="function">php\_strip\_whitespace</span> -
    返回已经去除注释和空白的源代码 </span>
-   <span class="simpara"> <span class="function">proc\_nice</span> -
    修改当前进程的优前级 </span>
-   <span class="simpara"> <span
    class="function">pspell\_config\_data\_dir</span> -
    修改语言文件的位置 </span>
-   <span class="simpara"> <span
    class="function">pspell\_config\_dict\_dir</span> -
    修改主要单词列表的位置 </span>
-   <span class="simpara"> <span class="function">setrawcookie</span> -
    发送一个没有经过 url 编码的 cookie 值 </span>
-   <span class="simpara"> <span class="function">scandir</span> -
    列中指定目录中的所有子目录和文件 </span>
-   <span class="simpara"> <span
    class="function">snmp\_read\_mib</span> - 在一个可用的 MIB
    树中读取和分板一个 MIB 文件 </span>
-   <span class="simpara"> <span
    class="function">sqlite\_fetch\_column\_types</span> -
    以数组的形式返回一张表中的列类型 </span>

> **Note**:
>
> <a href="/ref/tidy.html" class="link">Tidy</a> 扩展库的 API
> 也作了重大调整
