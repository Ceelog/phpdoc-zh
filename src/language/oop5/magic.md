魔术方法
--------

<a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>，
<a href="/language/oop5/decon.html#object.destruct" class="link">__destruct()</a>，
<a href="/language/oop5/overloading.html#object.call" class="link">__call()</a>，
<a href="/language/oop5/overloading.html#object.callstatic" class="link">__callStatic()</a>，
<a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>，
<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>，
<a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>，
<a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a>，
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>，
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>，
<a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>,
<a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>,
<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>，
<a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>，
<a href="/language/oop5/magic.html#object.set-state" class="link">__set_state()</a>，
<a href="/language/oop5/cloning.html#object.clone" class="link">__clone()</a>
和
<a href="/language/oop5/magic.html#object.debuginfo" class="link">__debugInfo()</a>
等方法在 PHP 中被称为“魔术方法”（Magic
methods）。在命名自己的类方法时不能使用这些方法名，除非是想使用其魔术功能。

> **Note**: <span class="simpara"> 所有的魔术方法 *必须* 声明为 *public*
> </span>

**Caution**

PHP 将所有以
\_\_（两个下划线）开头的类方法保留为魔术方法。所以在定义类方法时，除了上述魔术方法，建议不要以
\_\_ 为前缀。

### <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a> 和 <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">\_\_sleep</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_wakeup</span> ( <span
class="methodparam">void</span> )

<span class="function">serialize</span>
函数会检查类中是否存在一个魔术方法
<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>。如果存在，该方法会先被调用，然后才执行序列化操作。此功能可以用于清理对象，并返回一个包含对象中所有应被序列化的变量名称的数组。如果该方法未返回任何内容，则
**`null`** 被序列化，并产生一个 **`E_NOTICE`** 级别的错误。

> **Note**:
>
> <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
> 不能返回父类的私有成员的名字。这样做会产生一个 **`E_NOTICE`**
> 级别的错误。可以用 <span class="classname">Serializable</span>
> 接口来替代。

<a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
方法常用于提交未提交的数据，或类似的清理操作。同时，如果有一些很大的对象，但不需要全部保存，这个功能就很好用。

与之相反，<span class="function">unserialize</span> 会检查是否存在一个
<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
方法。如果存在，则会先调用 *\_\_wakeup* 方法，预先准备对象需要的资源。

<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
经常用在反序列化操作中，例如重新建立数据库连接，或执行其它初始化操作。

**示例 \#1 Sleep 和 wakeup**

``` php
<?php
class Connection 
{
    protected $link;
    private $server, $username, $password, $db;
    
    public function __construct($server, $username, $password, $db)
    {
        $this->server = $server;
        $this->username = $username;
        $this->password = $password;
        $this->db = $db;
        $this->connect();
    }
    
    private function connect()
    {
        $this->link = mysql_connect($this->server, $this->username, $this->password);
        mysql_select_db($this->db, $this->link);
    }
    
    public function __sleep()
    {
        return array('server', 'username', 'password', 'db');
    }
    
    public function __wakeup()
    {
        $this->connect();
    }
}
?>
```

### <a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a> 和 <a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">\_\_serialize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_unserialize</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

<span class="function">serialize</span>
函数会检查类中是否存在一个魔术方法
<a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>。如果存在，该方法将在任何序列化之前优先执行。它必须以一个代表对象序列化形式的
键/值 成对的关联数组形式来返回，如果没有返回数组，将会抛出一个 <span
class="classname">TypeError</span> 错误。

> **Note**:
>
> 如果类中同时定义了
> <a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>
> 和
> <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
> 两个魔术方法，则只有
> <a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>
> 方法会被调用。
> <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
> 方法会被忽略掉。如果对象实现了
> <a href="/class/serializable.html" class="link">Serializable</a>
> 接口，接口的 *serialize()* 方法会被忽略，做为代替类中的
> <a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>
> 方法会被调用。

The intended use of
<a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>
is to define a serialization-friendly arbitrary representation of the
object. Elements of the array may correspond to properties of the object
but that is not required.

Conversely, <span class="function">unserialize</span> checks for the
presence of a function with the magic name
<a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>.
If present, this function will be passed the restored array that was
returned from
<a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>.
It may then restore the properties of the object from that array as
appropriate.

> **Note**:
>
> 如果类中同时定义了
> <a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>
> 和
> <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
> 两个魔术方法，则只有
> <a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>
> 方法会生效，<a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
> 方法会被忽略。

> **Note**:
>
> 此特性自 PHP 7.4.0 起可用。

**示例 \#2 序列化和反序列化**

``` php
<?php
class Connection
{
    protected $link;
    private $dsn, $username, $password;

    public function __construct($dsn, $username, $password)
    {
        $this->dsn = $dsn;
        $this->username = $username;
        $this->password = $password;
        $this->connect();
    }

    private function connect()
    {
        $this->link = new PDO($this->dsn, $this->username, $this->password);
    }

    public function __serialize(): array
    {
        return [
          'dsn' => $this->dsn,
          'user' => $this->username,
          'pass' => $this->password,
        ];
    }

    public function __unserialize(array $data): void
    {
        $this->dsn = $data['dsn'];
        $this->username = $data['user'];
        $this->password = $data['pass'];

        $this->connect();
    }
}?>
```

### <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
方法用于一个类被当成字符串时应怎样回应。例如 *echo $obj;*
应该显示些什么。此方法必须返回一个字符串，否则将发出一条
**`E_RECOVERABLE_ERROR`** 级别的致命错误。

**Warning**

不能在
<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
方法中抛出异常。这么做会导致致命错误。

**示例 \#3 简单示例**

``` php
<?php
// Declare a simple class
class TestClass
{
    public $foo;

    public function __construct($foo) 
    {
        $this->foo = $foo;
    }

    public function __toString() {
        return $this->foo;
    }
}

$class = new TestClass('Hello');
echo $class;
?>
```

以上例程会输出：

    Hello

需要指出的是在 PHP 5.2.0
之前，<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
方法只有在直接使用于 <span class="function">echo</span> 或 <span
class="function">print</span> 时才能生效。PHP 5.2.0
之后，则可以在任何字符串环境生效（例如通过 <span
class="function">printf</span>，使用 *%s*
修饰符），但不能用于非字符串环境（如使用 *%d* 修饰符）。自 PHP 5.2.0
起，如果将一个未定义
<a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
方法的对象转换为字符串，会产生 **`E_RECOVERABLE_ERROR`** 级别的错误。

### <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>

<span class="type">mixed</span> <span
class="methodname">\_\_invoke</span> (\[ <span class="methodparam">
`$...`</span> \] )

当尝试以调用函数的方式调用一个对象时，<a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>
方法会被自动调用。

> **Note**:
>
> 本特性只在 PHP 5.3.0 及以上版本有效。

**示例 \#4 使用
<a href="/language/oop5/magic.html#object.invoke" class="link">__invoke()</a>**

``` php
<?php
class CallableClass 
{
    function __invoke($x) {
        var_dump($x);
    }
}
$obj = new CallableClass;
$obj(5);
var_dump(is_callable($obj));
?>
```

以上例程会输出：

    int(5)
    bool(true)

### <a href="/language/oop5/magic.html#object.set-state" class="link">__set_state()</a>

<span class="modifier">static</span> <span class="type">object</span>
<span class="methodname">\_\_set\_state</span> ( <span
class="methodparam"><span class="type">array</span> `$properties`</span>
)

自 PHP 5.1.0 起当调用 <span class="function">var\_export</span>
导出类时，此<a href="/language/oop5/static.html" class="link">静态</a>
方法会被调用。

本方法的唯一参数是一个数组，其中包含按 *array('property' =\> value,
...)* 格式排列的类属性。

**示例 \#5 使用
<a href="/language/oop5/magic.html#object.set-state" class="link">__set_state()</a>\>（PHP
5.1.0 起）**

``` php
<?php

class A
{
    public $var1;
    public $var2;

    public static function __set_state($an_array) // As of PHP 5.1.0
    {
        $obj = new A;
        $obj->var1 = $an_array['var1'];
        $obj->var2 = $an_array['var2'];
        return $obj;
    }
}

$a = new A;
$a->var1 = 5;
$a->var2 = 'foo';

eval('$b = ' . var_export($a, true) . ';'); // $b = A::__set_state(array(
                                            //    'var1' => 5,
                                            //    'var2' => 'foo',
                                            // ));
var_dump($b);

?>
```

以上例程会输出：

    object(A)#2 (2) {
      ["var1"]=>
      int(5)
      ["var2"]=>
      string(3) "foo"
    }

### <a href="/language/oop5/magic.html#object.debuginfo" class="link">__debugInfo()</a>

<span class="type">array</span> <span
class="methodname">\_\_debugInfo</span> ( <span
class="methodparam">void</span> )

This method is called by <span class="function">var\_dump</span> when
dumping an object to get the properties that should be shown. If the
method isn't defined on an object, then all public, protected and
private properties will be shown.

This feature was added in PHP 5.6.0.

**示例 \#6 Using
<a href="/language/oop5/magic.html#object.debuginfo" class="link">__debugInfo()</a>**

``` php
<?php
class C {
    private $prop;

    public function __construct($val) {
        $this->prop = $val;
    }

    public function __debugInfo() {
        return [
            'propSquared' => $this->prop ** 2,
        ];
    }
}

var_dump(new C(42));
?>
```

以上例程会输出：

    object(C)#1 (1) {
      ["propSquared"]=>
      int(1764)
    }
