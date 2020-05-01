PHP 7.3.x 中废弃的功能
----------------------

### PHP 核心中废弃的功能

#### 大小写不敏感的常量

大小写不敏感的常量声明现已被废弃。将 **`TRUE`** 作为第三个参数传递给
<span class="function">define</span>
将会导致一个废弃警告。大小写不敏感的使用（在读取时使用一个与声明时不同的大小写方式）也已被废弃。

#### 命名空间中的 assert()

废弃：在一个命名空间中声明一个名为 *assert()* 的函数。 <span
class="function">assert</span>
函数属于引擎特殊处理的情况，当在命名空间中使用相同名字去定义
函数时也许会导致不一致的行为。

#### 在字符串中搜索非字符串内容

废弃：将一个非字符串内容传递给字符串搜索函数。
在将来所有待搜索的内容都将被视为字符串，而不是 ASCII
编码值。如果需要依赖这个特性，你应该
要么显示地进行类型转换（转为字符串），或者显示地调用 <span
class="function">chr</span>。 以下是受到影响的方法：

-   <span class="simpara"><span class="function">strpos</span></span>
-   <span class="simpara"><span class="function">strrpos</span></span>
-   <span class="simpara"><span class="function">stripos</span></span>
-   <span class="simpara"><span class="function">strripos</span></span>
-   <span class="simpara"><span class="function">strstr</span></span>
-   <span class="simpara"><span class="function">strchr</span></span>
-   <span class="simpara"><span class="function">strrchr</span></span>
-   <span class="simpara"><span class="function">stristr</span></span>

#### Strip-Tags Streaming

<span class="function">fgetss</span> 函数和
<a href="/filters/string.html" class="link">string.strip_tags stream filter</a>
已经被废弃。这同样影响了 <span
class="methodname">SplFileObject::fgetss</span> 方法和 <span
class="function">gzgetss</span> 函数。

### Data Filtering

对于 **`FILTER_FLAG_SCHEME_REQUIRED`** 和
**`FILTER_FLAG_HOST_REQUIRED`** 常量的显示使用已被废弃。
总之，**`FILTER_VALIDATE_URL`** 已经隐含了这两者。

### 图像处理和 GD 库

<span class="function">image2wbmp</span> 已被废弃。

### 国际化相关函数

如果 PHP 关联的ICU ≥ 56, 那么 **`Normalizer::NONE`**
形式的使用将会导致抛出一个废弃警告。

### 多字节字符串

以下在文档中不存在的 *mbereg\_\*()* 别名已被废弃。请使用相应的
*mb\_ereg\_\*()* 变体替代。

-   <span class="simpara"><span
    class="function">mbregex\_encoding</span></span>
-   <span class="simpara"><span class="function">mbereg</span></span>
-   <span class="simpara"><span class="function">mberegi</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_replace</span></span>
-   <span class="simpara"><span
    class="function">mberegi\_replace</span></span>
-   <span class="simpara"><span class="function">mbsplit</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_match</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_pos</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_regs</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_init</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_getregs</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_getpos</span></span>
-   <span class="simpara"><span
    class="function">mbereg\_search\_setpos</span></span>

### ODBC 和 DB2 函数 (PDO\_ODBC)

<a href="/book/pdo.html#" class="link">pdo_odbc.db2_instance_name</a>
ini 设置项在先前已被废弃。 它在文档中自 PHP 5.1.1 起被废弃
