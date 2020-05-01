不向下兼容的变化
----------------

尽管大多数现有的 PHP 5
代码无需改变就可以工作，但是请注意一些不向下兼容的变化：

-   <span class="simpara"> 在 PHP 5.3.x
    的所有绑定扩展中应用了新的内部参数解析API,
    当给函数传递了不兼容的参数时将返回 NULL. 但有一些例外，比如函数
    <span class="function">get\_class</span> 在出现错误时将会返回
    **`FALSE`**. </span>
-   <span class="simpara"> <span class="function">clearstatcache</span>
    默认不再清除缓存的 realpath. </span>
-   <span class="simpara"> <span class="function">realpath</span>
    现在是完全与平台无关的. 结果是非法的相对路径比如 *\_\_FILE\_\_ .
    "/../x"* 将不会工作. </span>
-   <span class="simpara"> <span
    class="function">call\_user\_func</span>
    系列函数即使被调用者是一个父类也使用 $this. </span>
-   <span class="simpara"> 数组函数 <span
    class="function">natsort</span>, <span
    class="function">natcasesort</span>, <span
    class="function">usort</span>, <span class="function">uasort</span>,
    <span class="function">uksort</span>, <span
    class="function">array\_flip</span>, 和 <span
    class="function">array\_unique</span> 将不再接受对象作为参数.
    在将这些函数应用于对象时, 请首先将对象转换为数组. </span>
-   <span class="simpara">
    按引用传递参数的函数在被按值传递调用时行为发生改变.
    此前函数将接受按值传递的参数, 现在将抛出致命错误.
    之前任何期待传递引用但是在调用时传递了常量或者字面值 的函数,
    需要在调用前改为将该值赋给一个变量。 </span>
-   <span class="simpara"> 新的 mysqlnd 库需要使用 MySQL 4.1 新的 41
    字节密码格式。继续使用旧的 16 字节密码将导致 <span
    class="function">mysql\_connect</span> 和其它类似函数 抛出 *"mysqlnd
    cannot connect to MySQL 4.1+ using old authentication."* 错误.
    </span>
-   <span class="simpara"> 新的 mysqlnd 库将不再读取 MySQL
    配置文件(my.cnf/my.ini), 这与旧版本的 libmysql 库不同.
    如果你的代码依赖于这些配置 文件, 你可以使用 <span
    class="function">mysqli\_options</span> 显式地加载它. 注意,
    这意味着如果 PDO 中的 MySQL 支持使用了 mysqlnd 进行编译，PDO
    特有常量 **`PDO::MYSQL_ATTR_READ_DEFAULT_FILE`** 和
    **`PDO::MYSQL_ATTR_READ_DEFAULT_GROUP`** 将是未定义的. </span>
-   <span class="simpara"> <span class="classname">SplFileInfo</span>
    及其相关目录类会移除末尾的 /. </span>
-   <span class="simpara">
    <a href="/language/oop5/magic.html#language.oop5.magic.tostring" class="link">__toString</a>
    魔术方法不再接受参数. </span>
-   <span class="simpara"> 魔术方法
    <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link">__get</a>,
    <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link">__set</a>,
    <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link">__isset</a>,
    <a href="/language/oop5/overloading.html#language.oop5.overloading.members" class="link">__unset</a>,
    and
    <a href="/language/oop5/overloading.html#language.oop5.overloading.methods" class="link">__call</a>
    应该总是公共的(public)且不能是静态的(static). 方法签名是必须的.
    </span>
-   <span class="simpara"> 现在
    <a href="/language/oop5/overloading.html#language.oop5.overloading.methods" class="link">__call</a>
    魔术方法在访问私有的(private)和被保护的(protected)方法时被调用.
    </span>
-   <span class="simpara"> 函数内 <span class="function">include</span>
    或者 <span class="function">require</span> 一个文件时，文件内
    将不能使用 <span class="function">func\_get\_arg</span>, <span
    class="function">func\_get\_args</span> 和 <span
    class="function">func\_num\_args</span> 函数。 </span>
-   <span class="simpara"> 新增了一个包裹在 MHASH
    扩展外面的仿真层。但是并非所有的算法都涉及到了，值得注意的是 s2k
    哈希算法。这意味着 s2k 哈希算法在 PHP 5.3.0 中不再可用。 </span>

以下关键词被保留，将不能被用作函数名, 类名等。

-   <span class="simpara">
    <a href="/control-structures/goto.html" class="link">goto</a>
    </span>
-   <span class="simpara">
    <a href="/language/namespaces.html" class="link">namespace</a>
    </span>
