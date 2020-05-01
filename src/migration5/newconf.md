新指令
------

PHP 5 在 `php.ini` 中引进了一些新指令。列表如下：

-   <span class="simpara"> mail.force\_extra\_parameters -
    强制指定的参数附加值作为额外的参数传递给 sendmail
    库。这些参数总是会替换掉 <span class="function">mail</span> 的第 5
    个参数，即使在安全模式下 </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>
    - 允许／禁止 PHP 注册已过时的 $HTTP\_\*\_VARS 变量 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.hash_function</a>
    - 选择一种散列函数（MD5 或 SHA-1） </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.hash_bits_per_character</a>
    - 定义将二进制散列数据转换为可读格式时每个字符中储存几个位（从 4 到
    6） </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.zend.ze1-compatibility-mode" class="link">zend.ze1_compatibility_mode</a>
    - 启用 Zend Engline 1 代（PHP 4）兼容模式 </span>
