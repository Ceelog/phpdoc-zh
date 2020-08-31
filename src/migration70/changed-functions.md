变更的函数
----------

### PHP 核心

-   <span class="simpara"> <span
    class="function">debug\_zval\_dump</span> 现在打印 "int" 替代
    "long", 打印 "float" 替代 "double" </span>
-   <span class="simpara"> <span class="function">dirname</span>
    增加了可选的第二个参数, `depth`, 获取当前目录向上 `depth`
    级父目录的名称。 </span>
-   <span class="simpara"> <span class="function">getrusage</span>
    现在支持 Windows. </span>
-   <span class="simpara"> <span class="function">mktime</span> and
    <span class="function">gmmktime</span> 函数不再接受 `is_dst` 参数。
    </span>
-   <span class="simpara"> <span class="function">preg\_replace</span>
    函数不再支持 "\\e" (**`PREG_REPLACE_EVAL`**). 应当使用 <span
    class="function">preg\_replace\_callback</span> 替代。 </span>
-   <span class="simpara"> <span class="function">setlocale</span>
    函数不再接受 `category` 传入字符串。 应当使用 **`LC_*`** 常量。
    </span>
-   <span class="simpara"> <span class="function">exec</span>, <span
    class="function">system</span> and <span
    class="function">passthru</span> 函数对 NULL 增加了保护. </span>
-   <span class="simpara"> <span class="function">shmop\_open</span>
    现在返回一个资源而非一个int， 这个资源可以传给<span
    class="function">shmop\_size</span>, <span
    class="function">shmop\_write</span>, <span
    class="function">shmop\_read</span>, <span
    class="function">shmop\_close</span> 和 <span
    class="function">shmop\_delete</span>. </span>
-   <span class="simpara"> <span class="function">substr</span> 现在当
    start 的值与 string 的长度相同时将返回一个空字符串。 </span>
-   <span class="simpara"> <span
    class="function">xml\_parser\_free</span>不再足以释放解析器资源，如果它引用了一个对象，而这个对象又引用了那个解析器资源。在这种情况下，需要额外地取消设置
    $parser。 </span>
