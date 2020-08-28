怎样修改配置设定
----------------

### PHP 运行于 Apache 模块方式

当使用 PHP 作为 Apache 模块时，也可以用 Apache 的配置文件（例如
`httpd.conf`）和 `.htaccess` 文件中的指令来修改 PHP
的配置设定。需要有“AllowOverride Options”或“AllowOverride
All”权限才可以。

有几个 Apache 指令可以使用户在 Apache 配置文件内部修改 PHP
的配置。哪些指令属于 **`PHP_INI_ALL`**，**`PHP_INI_PERDIR`** 或
**`PHP_INI_SYSTEM`** 中的哪一个，请参考附录中的
<a href="/ini/list.html" class="link">php.ini 配置选项列表</a>。

`php_value` `name` `value`  
设定指定的值。只能用于 **`PHP_INI_ALL`** 或 **`PHP_INI_PERDIR`**
类型的指令。要清除先前设定的值，把 value 设为 *none*。

> **Note**: <span class="simpara"> 不要用 `php_value` 设定布尔值。应该用
> `php_flag`（见下面）。 </span>

`php_flag` `name` `on|off`  
用来设定布尔值的配置指令。仅能用于 **`PHP_INI_ALL`** 和
**`PHP_INI_PERDIR`** 类型的指令。

`php_admin_value` `name` `value`  
设定指定的指令的值。*不能用于* `.htaccess` 文件。任何用
`php_admin_value` 设定的指令都不能被 `.htaccess` 或 virtualhost
中的指令覆盖。要清除先前设定的值，把 value 设为 *none*。

`php_admin_flag` `name` `on|off`  
用来设定布尔值的配置指令。*不能用于* `.htaccess` 文件。任何用
`php_admin_flag` 设定的指令都不能被 `.htaccess` 或 virtualhost
中的指令覆盖。

**示例 \#1 Apache 配置例子**

``` ini
<IfModule mod_php5.c>
  php_value include_path ".:/usr/local/lib/php"
  php_admin_flag engine on
</IfModule>
<IfModule mod_php4.c>
  php_value include_path ".:/usr/local/lib/php"
  php_admin_flag engine on
</IfModule>
```

**Caution**

PHP 常量不存在于 PHP 之外。例如在 `httpd.conf` 中不能使用 PHP 常量如
**`E_ALL`** 或 **`E_NOTICE`** 来设定
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
指令，因为其无意义，实际等于
*0*。应该用相应的掩码值来替代。这些常量可以在 `php.ini` 中使用。

### 通过 Windows 注册表修改 PHP 配置

在 Windows 下运行 PHP 时，可以用 Windows
注册表以目录为单位来修改配置。配置值存放于注册表项
*HKLM\\SOFTWARE\\PHP\\Per Directory Values*
下面，子项对应于路径名。例如对于目录 *c:\\inetpub\\wwwroot*
的配置值会存放于 *HKLM\\SOFTWARE\\PHP\\Per Directory
Values\\c\\inetpub\\wwwroot*
项下面。其中的设定对于任何位于此目录及其任何子目录的脚本都有效。项中的值的名称是
PHP 配置指令的名字，值的数据是字符串格式的指令值。值中的 PHP
常量不被解析。不过只有可修改范围是 **`PHP_INI_USER`**
的配置值可以用此方法设定，**`PHP_INI_PERDIR`**
的值就不行。因为这些配置对于每次请求来说是只读的。

### 其它接口下的 PHP

无论怎样运行 PHP，都可以在脚本中通过 <span
class="function">ini\_set</span> 而在运行时修改某个值。更多信息见手册中
<span class="function">ini\_set</span> 的页面。

如果对自己系统中的配置设定及其当前值的完整列表感兴趣，可以运行 <span
class="function">phpinfo</span> 函数并查看其结果的页面。也可以在运行时用
<span class="function">ini\_get</span> 或 <span
class="function">get\_cfg\_var</span> 取得个别配置指令的值。
