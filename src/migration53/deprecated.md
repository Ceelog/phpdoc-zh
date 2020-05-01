PHP 5.3.x 中弃用的功能
----------------------

PHP 5.3.0 新增了两个错误等级: **`E_DEPRECATED`** 和
**`E_USER_DEPRECATED`**. 错误等级 **`E_DEPRECATED`**
被用来说明一个函数或者功能已经被弃用. **`E_USER_DEPRECATED`**
等级目的在于表明用户代码中的弃用功能, 类似于 **`E_USER_ERROR`** 和
**`E_USER_WARNING`** 等级.

下面是被弃用的 INI 指令列表. 使用下面任何指令都将导致 **`E_DEPRECATED`**
错误.

-   <span class="simpara">
    <a href="/network/setup.html#" class="link">define_syslog_variables</a>
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>
    </span>
-   <span class="simpara">
    <a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
    </span>
-   <span class="simpara">
    <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
    </span>
-   <span class="simpara">
    <a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
    </span>
-   <span class="simpara">
    <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>
    </span>
-   <span class="simpara"> 弃用 INI 文件中以 '\#' 开头的注释. </span>

弃用函数:

-   <span class="simpara"> <span
    class="function">call\_user\_method</span> (使用 <span
    class="function">call\_user\_func</span> 替代) </span>
-   <span class="simpara"> <span
    class="function">call\_user\_method\_array</span> (使用 <span
    class="function">call\_user\_func\_array</span> 替代) </span>
-   <span class="simpara"> <span
    class="function">define\_syslog\_variables</span> </span>
-   <span class="simpara"> <span class="function">dl</span> </span>
-   <span class="simpara"> <span class="function">ereg</span> (使用
    <span class="function">preg\_match</span> 替代) </span>
-   <span class="simpara"> <span class="function">ereg\_replace</span>
    (使用 <span class="function">preg\_replace</span> 替代) </span>
-   <span class="simpara"> <span class="function">eregi</span> (使用
    <span class="function">preg\_match</span> 配合 *'i'* 修正符替代)
    </span>
-   <span class="simpara"> <span class="function">eregi\_replace</span>
    (使用 <span class="function">preg\_replace</span> 配合 *'i'*
    修正符替代) </span>
-   <span class="simpara"> <span
    class="function">set\_magic\_quotes\_runtime</span> 以及它的别名函数
    <span class="function">magic\_quotes\_runtime</span> </span>
-   <span class="simpara"> <span
    class="function">session\_register</span> (使用 `$_SESSION`
    超全部变量替代) </span>
-   <span class="simpara"> <span
    class="function">session\_unregister</span> (使用 `$_SESSION`
    超全部变量替代) </span>
-   <span class="simpara"> <span
    class="function">session\_is\_registered</span> (使用 `$_SESSION`
    超全部变量替代) </span>
-   <span class="simpara"> <span
    class="function">set\_socket\_blocking</span> (使用 <span
    class="function">stream\_set\_blocking</span> 替代) </span>
-   <span class="simpara"> <span class="function">split</span> (使用
    <span class="function">preg\_split</span> 替代) </span>
-   <span class="simpara"> <span class="function">spliti</span> (使用
    <span class="function">preg\_split</span> 配合 *'i'* 修正符替代)
    </span>
-   <span class="simpara"> <span class="function">sql\_regcase</span>
    </span>
-   <span class="simpara"> <span
    class="function">mysql\_db\_query</span> (使用 <span
    class="function">mysql\_select\_db</span> 和 <span
    class="function">mysql\_query</span> 替代) </span>
-   <span class="simpara"> <span
    class="function">mysql\_escape\_string</span> (使用 <span
    class="function">mysql\_real\_escape\_string</span> 替代) </span>
-   <span class="simpara"> 废弃以字符串传递区域设置名称. 使用 LC\_\*
    系列常量替代. </span>
-   <span class="simpara"> <span class="function">mktime</span> 的
    `is_dst` 参数. 使用新的时区处理函数替代. </span>

弃用的功能:

-   <span class="simpara"> 弃用通过引用分配
    <a href="/language/oop5/basic.html#language.oop5.basic.new" class="link">new</a>
    的返回值. </span>
-   <span class="simpara"> 调用时传递引用被弃用. </span>
