新特性
------

### 新的对象类型

这种新的对象类型, <span class="type">object</span>,
引进了可用于逆变（contravariant）参数输入和协变（covariant）返回任何对象类型。

``` php
<?php

function test(object $obj) : object
{
    return new SplQueue();
}

test(new StdClass());
```

### 通过名称加载扩展

扩展文件不再需要通过文件加载 (Unix下以*.so*为文件扩展名，在Windows下以
*.dll* 为文件扩展名) 进行指定。可以在php.ini配置文件进行启用, 也可以使用
<span class="function">dl</span> 函数进行启用。

### 允许重写抽象方法(Abstract method)

当一个抽象类继承于另外一个抽象类的时候，继承后的抽象类可以重写被继承的抽象类的抽象方法。

``` php
<?php

abstract class A
{
    abstract function test(string $s);
}
abstract class B extends A
{
    // overridden - still maintaining contravariance for parameters and covariance for return
    abstract function test($s) : int;
}
```

### 使用Argon2算法生成密码散列

Argon2 已经被加入到密码散列（password hashing） API (这些函数以
*password\_* 开头), 以下是暴露出来的常量:

-   <span class="simpara"> **`PASSWORD_ARGON2I`** </span>
-   <span class="simpara"> **`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**
    </span>
-   <span class="simpara"> **`PASSWORD_ARGON2_DEFAULT_TIME_COST`**
    </span>
-   <span class="simpara"> **`PASSWORD_ARGON2_DEFAULT_THREADS`** </span>

### 新增 ext/PDO（PDO扩展） 字符串扩展类型

当你准备支持多语言字符集，PDO的字符串类型已经扩展支持国际化的字符集。以下是扩展的常量：

-   <span class="simpara"> **`PDO::PARAM_STR_NATL`** </span>
-   <span class="simpara"> **`PDO::PARAM_STR_CHAR`** </span>
-   <span class="simpara"> **`PDO::ATTR_DEFAULT_STR_PARAM`** </span>

这些常量通过**`PDO::PARAM_STR`**利用位运算*OR*进行计算：

``` php
<?php

$db->quote('über', PDO::PARAM_STR | PDO::PARAM_STR_NATL);
```

### 为 ext/PDO新增额外的模拟调试信息

<span
class="function">PDOStatement::debugDumpParams</span>方法已经更新，当发送SQL到数据库的时候，在一致性、行查询（包括替换绑定占位符）将会显示调试信息。这一特性已经加入到模拟调试中（在模拟调试打开时可用）。

### ext/LDAP（LDAP扩展） 支持新的操作方式

LDAP 扩展已经新增了EXOP支持. 扩展暴露以下函数和常量:

-   <span class="simpara"> <span
    class="function">ldap\_parse\_exop</span> </span>
-   <span class="simpara"> <span class="function">ldap\_exop</span>
    </span>
-   <span class="simpara"> <span
    class="function">ldap\_exop\_passwd</span> </span>
-   <span class="simpara"> <span
    class="function">ldap\_exop\_whoami</span> </span>
-   <span class="simpara"> **`LDAP_EXOP_START_TLS`** </span>
-   <span class="simpara"> **`LDAP_EXOP_MODIFY_PASSWD`** </span>
-   <span class="simpara"> **`LDAP_EXOP_REFRESH`** </span>
-   <span class="simpara"> **`LDAP_EXOP_WHO_AM_I`** </span>
-   <span class="simpara"> **`LDAP_EXOP_TURN`** </span>

### ext/sockets（sockets扩展）添加了地址信息

sockets扩展现在具有查找地址信息的能力，且可以连接到这个地址，或者进行绑定和解析。为此添加了以下一些函数:

-   <span class="simpara"> <span
    class="function">socket\_addrinfo\_lookup</span> </span>
-   <span class="simpara"> <span
    class="function">socket\_addrinfo\_connect</span> </span>
-   <span class="simpara"> <span
    class="function">socket\_addrinfo\_bind</span> </span>
-   <span class="simpara"> <span
    class="function">socket\_addrinfo\_explain</span> </span>

### 扩展了参数类型

重写方法和接口实现的参数类型现在可以省略了。不过这仍然是符合LSP，因为现在这种参数类型是逆变的。

``` php
<?php

interface A
{
    public function Test(array $input);
}

class B implements A
{
    public function Test($input){} // type omitted for $input
}
```

### 允许分组命名空间的尾部逗号

命名空间可以在PHP 7中使用尾随逗号进行分组引入。

``` php
<?php

use Foo\Bar\{
    Foo,
    Bar,
    Baz,
};
```
