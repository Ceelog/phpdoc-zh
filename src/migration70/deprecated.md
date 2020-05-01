PHP 7.0.x 弃用的功能
--------------------

### PHP4 风格的构造函数

PHP4 风格的构造函数（方法名和类名一样）将被弃用，并在将来移除。
如果在类中仅使用了 PHP4 风格的构造函数，PHP7 会产生 **`E_DEPRECATED`**
警告。 如果还定义了 <span class="function">\_\_construct</span>
方法则不受影响。

``` php
<?php
class foo {
    function foo() {
        echo 'I am the constructor';
    }
}
?>
```

以上例程会输出：

    Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; foo has a deprecated constructor in example.php on line 3

### 静态调用非静态的方法

废弃了
<a href="/language/oop5/static.html" class="link">静态（Static）</a>
调用未声明成 **static** 的方法，未来可能会彻底移除该功能。

``` php
<?php
class foo {
    function bar() {
        echo 'I am not static!';
    }
}

foo::bar();
?>
```

以上例程会输出：

    Deprecated: Non-static method foo::bar() should not be called statically in - on line 8
    I am not static!

### <span class="function">password\_hash</span> 盐值选项

废弃了 <span class="function">password\_hash</span>
函数中的盐值选项，阻止开发者生成自己的盐值（通常更不安全）。
开发者不传该值时，该函数自己会生成密码学安全的盐值。因此再无必要传入自己自定义的盐值。

### *capture\_session\_meta* SSL 上下文选项

废弃了 *capture\_session\_meta* 内的 SSL 上下文选项。 现在可以通过 <span
class="function">stream\_get\_meta\_data</span> 获取 SSL
元数据（metadata）。

### <a href="/book/ldap.html" class="link">LDAP</a> 中的废弃

以下函数已被废弃：

-   <span class="simpara"> <span class="function">ldap\_sort</span>
    </span>
