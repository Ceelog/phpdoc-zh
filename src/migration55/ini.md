INI 文件处理的变化
------------------

### <a href="/book/intl.html" class="link">Intl</a>

新增 *intl.use\_exceptions* 配置指令，当发生全局错误时，连同已经现存的
*intl.error\_level* 配置指令一起用来控制 intl 的行为。

### <a href="/set/mysqlinfo.html#Mysqlnd" class="link">MySQLnd</a>

新增 *mysqlnd.sha256\_server\_public\_key* 配置指令来允许
<a href="/set/mysqlinfo.html#Mysqli" class="link">mysqli</a>
使用新的MySQL 认证协议。
