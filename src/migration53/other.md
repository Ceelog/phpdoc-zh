其他改变
--------

-   <span class="simpara"> <span
    class="function">SplFileInfo::getpathinfo</span> 现在返回 path name
    信息. </span>
-   <span class="simpara"> <span
    class="classname">SplObjectStorage</span> 现在支持 <span
    class="classname">ArrayAccess</span>。现在可以在 <span
    class="classname">SplObjectStorage</span> 中存储关联信息对象.
    </span>
-   <span class="simpara"> 在 GD 扩展中，通过 <span
    class="function">imagefilter</span> 函数，可以提供像素支持. </span>
-   <span class="simpara"> <span class="function">var\_dump</span>
    的输出现在包含对象的私有属性. </span>
-   <span class="simpara"> 如果会话启动失败，<span
    class="function">session\_start</span> 现在将返回 **`false`**.
    </span>
-   <span class="simpara"> <span
    class="function">property\_exists</span>
    可以检查一个属性的存在性，而不管它的访问控制类型(类似于 <span
    class="function">method\_exists</span>). </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.include-path" class="link">include_path</a>
    现在可以使用<a href="/wrappers.html" class="link">Stream 包装器</a>。
    </span>
-   <span class="simpara"> <span class="function">array\_reduce</span>
    函数的 `initial` 参数现在可以是任何类型. </span>
-   <span class="simpara">
    如果没有明确传递上下文环境，<a href="/ref/dir.html" class="link">目录函数</a>
    <span class="function">opendir</span>，<span
    class="function">scandir</span>，和 <span
    class="function">dir</span> 将使用默认的流上下文环境. </span>
-   <span class="simpara"> <span class="function">crypt</span> 函数支持
    Blowfish 和 DES 算法，并且 <span class="function">crypt</span>
    的特点是非常便捷。 PHP 有它自己内部的算法实现，不管是否找到 *crypt*
    或 *crypt\_r*。 </span>
-   <span class="simpara"> 在全部平台上，<span
    class="function">getopt</span>
    开始接受"长选项"。可选值和作为短选项分隔符的 *=* 被支持. </span>
-   <span class="simpara"> <span class="function">fopen</span>
    新增了一个模式选项(*n*)，它传递 **`O_NONBLOCK`** 常量给底层的
    *open()* 系统调用。注意，Windows 上该模式尚未得到支持。 </span>
-   <span class="simpara"> <span class="function">getimagesize</span>
    现在支持 icon 文件 (.ico). </span>
-   <span class="simpara"> mhash 扩展已经移动至 PECL，但如果 PHP 使用
    *--with-mhash*
    选项参数进行编译，<a href="/ref/hash.html" class="link">Hash</a>
    扩展也将提供 mhash 支持。注意，不管是否开启 mhash 算法，Hash
    扩展都无需 mhash 库可用。 </span>
