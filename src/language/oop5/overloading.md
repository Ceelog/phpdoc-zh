重载
----

PHP所提供的“重载”（overloading）是指动态地“创建”类属性和方法。我们是通过魔术方法（magic
methods）来实现的。

当调用当前环境下未定义或不<a href="/language/oop5/visibility.html" class="link">可见</a>的类属性或方法时，重载方法会被调用。本节后面将使用“不可访问属性（inaccessible
properties）”和“不可访问方法（inaccessible
methods）”来称呼这些未定义或不可见的类属性或方法。

所有的重载方法都必须被声明为 *public*。

> **Note**:
>
> 这些魔术方法的参数都不能<a href="/functions/arguments.html#functions.arguments.by-reference" class="link">通过引用传递</a>。

> **Note**:
>
> PHP中的“重载”与其它绝大多数面向对象语言不同。传统的“重载”是用于提供多个同名的类方法，但各方法的参数类型和个数不同。

### 更新日志

| 版本  | 说明                                                                                                                                                                                       |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 新增 <a href="/language/oop5/overloading.html#object.callstatic" class="link">__callStatic()</a>魔术方法。可见性未设置为 public 或未声明为 static 的时候会产生一个警告。                   |
| 5.1.0 | 新增 <a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a> 和 <a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a> 两个魔术方法。 |

### 属性重载

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_get</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">\_\_isset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">\_\_unset</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

在给不可访问属性赋值时，<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>
会被调用。

读取不可访问属性的值时，<a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>
会被调用。

当对不可访问属性调用 <span class="function">isset</span> 或 <span
class="function">empty</span>
时，<a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
会被调用。

当对不可访问属性调用 <span class="function">unset</span>
时，<a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a>
会被调用。

参数 `$name`
是指要操作的变量名称。<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>
方法的 `$value` 参数指定了 `$name` 变量的值。

属性重载只能在对象中进行。在静态方法中，这些魔术方法将不会被调用。所以这些方法都不能被
声明为 <a href="/language/oop5/static.html" class="link">static</a>。从
PHP 5.3.0 起, 将这些魔术方法定义为 *static* 会产生一个警告。

> **Note**:
>
> 因为 PHP
> 处理赋值运算的方式，<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>
> 的返回值将被忽略。类似的,
> 在下面这样的链式赋值中，<a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>
> 不会被调用：
>
>      $a = $obj->b = 8; 

> **Note**:
>
> 在除 <span class="function">isset</span>
> 外的其它语言结构中无法使用重载的属性，这意味着当对一个重载的属性使用
> <span class="function">empty</span> 时，重载魔术方法将不会被调用。
>
> 为避开此限制，必须将重载属性赋值到本地变量再使用 <span
> class="function">empty</span>。

**示例 \#1 使用
<a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>，<a href="/language/oop5/overloading.html#object.set" class="link">__set()</a>，<a href="/language/oop5/overloading.html#object.isset" class="link">__isset()</a>
和
<a href="/language/oop5/overloading.html#object.unset" class="link">__unset()</a>
进行属性重载**

``` php
<?php
class PropertyTest {
     /**  被重载的数据保存在此  */
    private $data = array();

 
     /**  重载不能被用在已经定义的属性  */
    public $declared = 1;

     /**  只有从类外部访问这个属性时，重载才会发生 */
    private $hidden = 2;

    public function __set($name, $value) 
    {
        echo "Setting '$name' to '$value'\n";
        $this->data[$name] = $value;
    }

    public function __get($name) 
    {
        echo "Getting '$name'\n";
        if (array_key_exists($name, $this->data)) {
            return $this->data[$name];
        }

        $trace = debug_backtrace();
        trigger_error(
            'Undefined property via __get(): ' . $name .
            ' in ' . $trace[0]['file'] .
            ' on line ' . $trace[0]['line'],
            E_USER_NOTICE);
        return null;
    }

    /**  PHP 5.1.0之后版本 */
    public function __isset($name) 
    {
        echo "Is '$name' set?\n";
        return isset($this->data[$name]);
    }

    /**  PHP 5.1.0之后版本 */
    public function __unset($name) 
    {
        echo "Unsetting '$name'\n";
        unset($this->data[$name]);
    }

    /**  非魔术方法  */
    public function getHidden() 
    {
        return $this->hidden;
    }
}


echo "<pre>\n";

$obj = new PropertyTest;

$obj->a = 1;
echo $obj->a . "\n\n";

var_dump(isset($obj->a));
unset($obj->a);
var_dump(isset($obj->a));
echo "\n";

echo $obj->declared . "\n\n";

echo "Let's experiment with the private property named 'hidden':\n";
echo "Privates are visible inside the class, so __get() not used...\n";
echo $obj->getHidden() . "\n";
echo "Privates not visible outside of class, so __get() is used...\n";
echo $obj->hidden . "\n";
?>
```

以上例程会输出：

    Setting 'a' to '1'
    Getting 'a'
    1

    Is 'a' set?
    bool(true)
    Unsetting 'a'
    Is 'a' set?
    bool(false)

    1

    Let's experiment with the private property named 'hidden':
    Privates are visible inside the class, so __get() not used...
    2
    Privates not visible outside of class, so __get() is used...
    Getting 'hidden'


    Notice:  Undefined property via __get(): hidden in <file> on line 70 in <file> on line 29

### 方法重载

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">\_\_call</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">array</span>
`$arguments`</span> )

<span class="modifier">public static</span> <span
class="type">mixed</span> <span class="methodname">\_\_callStatic</span>
( <span class="methodparam"><span class="type">string</span>
`$name`</span> , <span class="methodparam"><span
class="type">array</span> `$arguments`</span> )

在对象中调用一个不可访问方法时，<a href="/language/oop5/overloading.html#object.call" class="link">__call()</a>
会被调用。

在静态上下文中调用一个不可访问方法时，<a href="/language/oop5/overloading.html#object.callstatic" class="link">__callStatic()</a>
会被调用。

`$name` 参数是要调用的方法名称。`$arguments`
参数是一个枚举数组，包含着要传递给方法 `$name` 的参数。

**示例 \#2 使用
<a href="/language/oop5/overloading.html#object.call" class="link">__call()</a>
和
<a href="/language/oop5/overloading.html#object.callstatic" class="link">__callStatic()</a>
对方法重载**

``` php
<?php
class MethodTest 
{
    public function __call($name, $arguments) 
    {
        // 注意: $name 的值区分大小写
        echo "Calling object method '$name' "
             . implode(', ', $arguments). "\n";
    }

    /**  PHP 5.3.0之后版本  */
    public static function __callStatic($name, $arguments) 
    {
        // 注意: $name 的值区分大小写
        echo "Calling static method '$name' "
             . implode(', ', $arguments). "\n";
    }
}

$obj = new MethodTest;
$obj->runTest('in object context');

MethodTest::runTest('in static context');  // PHP 5.3.0之后版本
?>
```

以上例程会输出：

    Calling object method 'runTest' in object context
    Calling static method 'runTest' in static context
