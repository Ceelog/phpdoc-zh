INI 文件处理改变
----------------

PHP 5.3.0 显著改进了 INI 文件的性能和解析，并且新增了若干语法功能.

-   <span class="simpara"> 标准的 `php.ini` 文件被重新组织和命名。
    *php.ini-development*
    包含在开发环境中推荐使用的设置。*php.ini-production*
    包含在生产环境中推荐使用的设置. </span>
-   <span class="simpara"> 支持两个特殊章节:
    *\[PATH=/opt/httpd/www.example.com/\]* 和
    *\[HOST=www.example.com\]*。 这两个章节里的指令不能被用户定义的 INI
    文件或者运行时覆盖。
    关于这些章节的更多信息，可以<a href="/ini/sections.html" class="link">这里</a>找到.
    </span>
-   <span class="simpara"> 移除了 *zend\_extension\_debug* and
    *zend\_extension\_ts*。使用 *zend\_extension* 指令来加载全部 Zend
    扩展. </span>
-   <span class="simpara"> 移除了
    *zend.ze1\_compatibility\_mode*。如果该 INI 指令被设置为
    On，启动时将抛出 **`E_ERROR`** 级别错误。 </span>
-   <span class="simpara"> 在
    "<a href="/ini/core.html#ini.extension" class="link"><em>extension</em></a>"
    指令中可以使用全路径来加载模块. </span>
-   <span class="simpara"> *"ini变量"* 现在几乎在 `php.ini`
    文件的任何地方都可以使用。 </span>
-   <span class="simpara"> 可以在运行时收紧 *open\_basedir*
    限制条件，该配置的范围现在是 PHP\_INI\_ALL。 </span>
-   <span class="simpara"> 可以在 INI 选项数组中使用字母数字或者变量.
    </span>
-   <span class="simpara"> <span class="function">get\_cfg\_var</span>
    现在可以返回 "数组(array)" INI 选项. </span>
-   <span class="simpara"> 添加了两个新指令
    <a href="/mail/setup.html#" class="link">mail.add_x_header</a> 和
    <a href="/mail/setup.html#" class="link">mail.log</a>。 </span>

添加了以下新的 PHP ini 配置项：

-   <span class="simpara"> user\_ini.filename 是新增的. </span>
-   <span class="simpara"> user\_ini.cache\_ttl 也是新增的. </span>
-   <span class="simpara"> exit\_on\_timeout 也是新增的. </span>
-   <span class="simpara"> open\_basedir 现在是 PHP\_INI\_ALL 的.
    </span>

新增以下指令:

-   <span class="simpara"> 通过 *user\_ini.filename* 和
    *user\_ini.cache\_ttl* 控制
    <a href="/configuration/file/per-user.html" class="link">.user.ini 文件</a>。
    </span>
-   <span class="simpara"> 添加
    <a href="/ini/core.html#ini.exit-on-timeout" class="link">exit_on_timeout</a>
    控制 Apache 1.x 子进程当 PHP 执行超时强制退出。 </span>
-   <span class="simpara"> 新增
    *mbstring.http\_output\_conv\_mimetype*。 该指令指定了 <span
    class="function">mb\_output\_handler</span>
    激活内容类型的正则表达式。 </span>
-   <span class="simpara"> 新增 *request\_order*。
    允许控制哪些外部变量在 `$_REQUEST` 中可用。 </span>

以下 ini 指令修改了默认值:

-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.use_only_cookies</a>
    默认被设置为 *"1"*(打开). </span>
-   <span class="simpara">
    <a href="/book/oci8.html#" class="link">oci8.default_prefetch</a>
    变更为从 *"10"* 到 *"100"*。 </span>
