Trait
-----

自 PHP 5.4.0 起，PHP 实现了一种代码复用的方法，称为 trait。

Trait 是为类似 PHP 的单继承语言而准备的一种代码复用机制。Trait
为了减少单继承语言的限制，使开发人员能够自由地在不同层次结构内独立的类中复用
method。Trait 和 Class
组合的语义定义了一种减少复杂性的方式，避免传统多继承和 Mixin
类相关典型问题。

Trait 和 Class 相似，但仅仅旨在用细粒度和一致的方式来组合功能。 无法通过
trait
自身来实例化。它为传统继承增加了水平特性的组合；也就是说，应用的几个
Class 之间不需要继承。

**示例 \#1 Trait 示例**

``` php
<?php
trait ezcReflectionReturnInfo {
    function getReturnType() { /*1*/ }
    function getReturnDescription() { /*2*/ }
}

class ezcReflectionMethod extends ReflectionMethod {
    use ezcReflectionReturnInfo;
    /* ... */
}

class ezcReflectionFunction extends ReflectionFunction {
    use ezcReflectionReturnInfo;
    /* ... */
}
?>
```

### 优先级

从基类继承的成员会被 trait
插入的成员所覆盖。优先顺序是来自当前类的成员覆盖了 trait 的方法，而
trait 则覆盖了被继承的方法。

**示例 \#2 优先顺序示例**

从基类继承的成员被插入的 SayWorld Trait 中的 MyHelloWorld
方法所覆盖。其行为 MyHelloWorld
类中定义的方法一致。优先顺序是当前类中的方法会覆盖 trait 方法，而 trait
方法又覆盖了基类中的方法。

``` php
<?php
class Base {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait SayWorld {
    public function sayHello() {
        parent::sayHello();
        echo 'World!';
    }
}

class MyHelloWorld extends Base {
    use SayWorld;
}

$o = new MyHelloWorld();
$o->sayHello();
?>
```

以上例程会输出：

    Hello World!

**示例 \#3 另一个优先级顺序的例子**

``` php
<?php
trait HelloWorld {
    public function sayHello() {
        echo 'Hello World!';
    }
}

class TheWorldIsNotEnough {
    use HelloWorld;
    public function sayHello() {
        echo 'Hello Universe!';
    }
}

$o = new TheWorldIsNotEnough();
$o->sayHello();
?>
```

以上例程会输出：

    Hello Universe!

### 多个 trait

通过逗号分隔，在 use 声明列出多个 trait，可以都插入到一个类中。

**示例 \#4 多个 trait 的用法**

``` php
<?php
trait Hello {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait World {
    public function sayWorld() {
        echo 'World';
    }
}

class MyHelloWorld {
    use Hello, World;
    public function sayExclamationMark() {
        echo '!';
    }
}

$o = new MyHelloWorld();
$o->sayHello();
$o->sayWorld();
$o->sayExclamationMark();
?>
```

以上例程会输出：

    Hello World!

### 冲突的解决

如果两个 trait
都插入了一个同名的方法，如果没有明确解决冲突将会产生一个致命错误。

为了解决多个 trait 在同一个类中的命名冲突，需要使用 *insteadof*
操作符来明确指定使用冲突方法中的哪一个。

以上方式仅允许排除掉其它方法，*as* 操作符可以 为某个方法引入别名。
注意，*as* 操作符不会对方法进行重命名，也不会影响其方法。

**示例 \#5 冲突的解决**

在本例中 Talker 使用了 trait A 和 B。由于 A 和 B
有冲突的方法，其定义了使用 trait B 中的 smallTalk 以及 trait A 中的
bigTalk。

Aliased\_Talker 使用了 *as* 操作符来定义了 *talk* 来作为 B 的 bigTalk
的别名。

``` php
<?php
trait A {
    public function smallTalk() {
        echo 'a';
    }
    public function bigTalk() {
        echo 'A';
    }
}

trait B {
    public function smallTalk() {
        echo 'b';
    }
    public function bigTalk() {
        echo 'B';
    }
}

class Talker {
    use A, B {
        B::smallTalk insteadof A;
        A::bigTalk insteadof B;
    }
}

class Aliased_Talker {
    use A, B {
        B::smallTalk insteadof A;
        A::bigTalk insteadof B;
        B::bigTalk as talk;
    }
}
?>
```

> **Note**:
>
> 在 PHP 7.0 之前，在类里定义和 trait
> 同名的属性，哪怕是完全兼容的也会抛出
> **`E_STRICT`**（完全兼容的意思：具有相同的访问可见性、初始默认值）。

### 修改方法的访问控制

使用 *as* 语法还可以用来调整方法的访问控制。

**示例 \#6 修改方法的访问控制**

``` php
<?php
trait HelloWorld {
    public function sayHello() {
        echo 'Hello World!';
    }
}

// 修改 sayHello 的访问控制
class MyClass1 {
    use HelloWorld { sayHello as protected; }
}

// 给方法一个改变了访问控制的别名
// 原版 sayHello 的访问控制则没有发生变化
class MyClass2 {
    use HelloWorld { sayHello as private myPrivateHello; }
}
?>
```

### 从 trait 来组成 trait

正如 class 能够使用 trait 一样，其它 trait 也能够使用 trait。在 trait
定义时通过使用一个或多个 trait，能够组合其它 trait 中的部分或全部成员。

**示例 \#7 从 trait 来组成 trait**

``` php
<?php
trait Hello {
    public function sayHello() {
        echo 'Hello ';
    }
}

trait World {
    public function sayWorld() {
        echo 'World!';
    }
}

trait HelloWorld {
    use Hello, World;
}

class MyHelloWorld {
    use HelloWorld;
}

$o = new MyHelloWorld();
$o->sayHello();
$o->sayWorld();
?>
```

以上例程会输出：

    Hello World!

### Trait 的抽象成员

为了对使用的类施加强制要求，trait 支持抽象方法的使用。

**示例 \#8 表示通过抽象方法来进行强制要求**

``` php
<?php
trait Hello {
    public function sayHelloWorld() {
        echo 'Hello'.$this->getWorld();
    }
    abstract public function getWorld();
}

class MyHelloWorld {
    private $world;
    use Hello;
    public function getWorld() {
        return $this->world;
    }
    public function setWorld($val) {
        $this->world = $val;
    }
}
?>
```

### Trait 的静态成员

Traits 可以被静态成员静态方法定义。

**示例 \#9 静态变量**

``` php
<?php
trait Counter {
    public function inc() {
        static $c = 0;
        $c = $c + 1;
        echo "$c\n";
    }
}

class C1 {
    use Counter;
}

class C2 {
    use Counter;
}

$o = new C1(); $o->inc(); // echo 1
$p = new C2(); $p->inc(); // echo 1
?>
```

**示例 \#10 静态方法**

``` php
<?php
trait StaticExample {
    public static function doSomething() {
        return 'Doing something';
    }
}

class Example {
    use StaticExample;
}

Example::doSomething();
?>
```

### 属性

Trait 同样可以定义属性。

**示例 \#11 定义属性**

``` php
<?php
trait PropertiesTrait {
    public $x = 1;
}

class PropertiesExample {
    use PropertiesTrait;
}

$example = new PropertiesExample;
$example->x;
?>
```

Trait 定义了一个属性后，类就不能定义同样名称的属性，否则会产生 fatal
error。 有种情况例外：属性是兼容的（同样的访问可见度、初始默认值）。 在
PHP 7.0 之前，属性是兼容的，则会有 E\_STRICT 的提醒。

**示例 \#12 解决冲突**

``` php
<?php
trait PropertiesTrait {
    public $same = true;
    public $different = false;
}

class PropertiesExample {
    use PropertiesTrait;
    public $same = true; // PHP 7.0.0 后没问题，之前版本是 E_STRICT 提醒
    public $different = true; // 致命错误
}
?>
```
