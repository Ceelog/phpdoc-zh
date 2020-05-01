新增的方法
----------

5.3.0 中新增了若干方法:

<a href="/book/datetime.html" class="link">日期/时间</a>:

-   <span class="simpara"> <span class="function">DateTime::add</span> -
    向一个 <span class="classname">DateTime</span> 对象加上若干天, 月,
    年, 小时, 分钟和秒. </span>
-   <span class="simpara"> <span
    class="function">DateTime::createFromFormat</span> - 根据给定的格式,
    返回一个新的格式化的<span class="classname">DateTime</span>对象.
    </span>
-   <span class="simpara"> <span
    class="function">DateTime::diff</span> - 返回两个 <span
    class="classname">DateTime</span> 对象的不同之处. </span>
-   <span class="simpara"> <span
    class="function">DateTime::getLastErrors</span> -
    返回最后的日期/时间处理中的警告和错误. </span>
-   <span class="simpara"> <span class="function">DateTime::sub</span> -
    从 <span class="classname">DateTime</span> 对象中减去若干天, 月, 年,
    小时, 分钟和秒. </span>

<span class="classname">异常(Exception)</span>:

-   <span class="simpara"> <span
    class="function">Exception::getPrevious</span> - 获取前一个异常.
    </span>

<a href="/book/dom.html" class="link">DOM</a>:

-   <span class="simpara"> <span
    class="function">DOMNode::getLineNo</span> - 返回解析节点的行数.
    </span>

<a href="/book/pdo.html#Firebird%20(PDO)" class="link">PDO_FIREBIRD</a>:

-   <span class="simpara"> <span
    class="function">PDO::setAttribute</span> - 设置属性. </span>

<a href="/book/reflection.html" class="link">反射(Reflection)</a>:

-   <span class="simpara"> <span
    class="methodname">ReflectionClass::getNamespaceName</span> -
    返回类定义所在命名空间的的名称. </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionClass::getShortName</span> -
    返回类的短名称(没有命名空间部分). </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionClass::inNamespace</span> -
    返回类是否定义于一个命名空间. </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionFunction::getNamespaceName</span> -
    返回函数定义所在命名空间的名字. </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionFunction::getShortName</span> -
    返回函数的段名称(没有命名空间部分). </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionFunction::inNamespace</span> -
    返回函数在一个命名空间中是否被定义. </span>
-   <span class="simpara"> <span
    class="methodname">ReflectionProperty::setAccessible</span> -
    设置是否可以请求非 public 属性. </span>

<a href="/book/spl.html" class="link">SPL</a>:

-   <span class="simpara"> <span
    class="function">SplObjectStorage::addAll</span> - 从另一个
    SplObjectStorage 对象中新增全部元素. </span>
-   <span class="simpara"> <span
    class="function">SplObjectStorage::removeAll</span> - 从另一个
    SplObjectStorage 对象中移除全部元素. </span>

<a href="/book/xsl.html" class="link">XSL</a>:

-   <span class="simpara"> <span
    class="function">XSLTProcessor::setProfiling</span> -
    设置概况输出文件. </span>
