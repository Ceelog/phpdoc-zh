PHP 5.5.x 中废弃的特性
----------------------

### 废弃 <a href="/set/mysqlinfo.html#Mysql（原始）" class="link">ext/mysql</a>

<a href="/set/mysqlinfo.html#Mysql（原始）" class="link">原始的 MySQL 扩展</a>
现在被废弃，当连接到数据库时会产生一个 **`E_DEPRECATED`** 错误。可使用
<a href="/set/mysqlinfo.html#Mysqli" class="link">MySQLi</a> 或
<a href="/book/pdo.html#MySQL%20(PDO)" class="link">PDO_MySQL</a>
扩展作为替代。

### <span class="function">preg\_replace</span> 中的 */e* 修饰符

<span class="function">preg\_replace</span> 函数中用到的 */e*
修饰符现在被弃用。可以使用 <span
class="function">preg\_replace\_callback</span> 函数来替代。

### <a href="/book/intl.html" class="link">intl</a> 中的废弃

<span class="methodname">IntlDateFormatter::setTimeZoneID</span> 和
<span class="function">datefmt\_set\_timezone\_id</span>
现在被废弃。可分别使用 <span
class="methodname">IntlDateFormatter::setTimeZone</span> 方法和 <span
class="function">datefmt\_set\_timezone</span> 函数作为替代。

### <a href="/book/mcrypt.html" class="link">mcrypt</a> 中的废弃

下列函数已被废弃：

-   <span class="simpara"> <span class="function">mcrypt\_cbc</span>
    </span>
-   <span class="simpara"> <span class="function">mcrypt\_cfb</span>
    </span>
-   <span class="simpara"> <span class="function">mcrypt\_ecb</span>
    </span>
-   <span class="simpara"> <span class="function">mcrypt\_ofb</span>
    </span>
