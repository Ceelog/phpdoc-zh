新特性
------

PHP 5.3.0 提供了广泛的新特性：

-   <span class="simpara"> 添加了
    <a href="/language/namespaces.html" class="link">命名空间</a>
    的支持. </span>
-   <span class="simpara"> 添加了
    <a href="/language/oop5/late-static-bindings.html" class="link">静态晚绑定</a>
    支持. </span>
-   <span class="simpara"> 添加了
    <a href="/control-structures/goto.html" class="link">跳转标签</a>
    (limited goto) 支持。 </span>
-   <span class="simpara"> 添加了原生的
    <a href="/functions/anonymous.html" class="link">闭包</a>
    (Lambda/匿名函数) 支持. </span>
-   <span class="simpara"> 新增了两个魔术方法,
    <a href="/language/oop5/overloading.html#object.callstatic" class="link">__callStatic</a>
    和
    <a href="/language/oop5/magic.html#object.invoke" class="link">__invoke</a>。
    </span>
-   <span class="simpara"> 添加了
    <a href="/language/types/string.html#language.types.string.syntax.nowdoc" class="link">Nowdoc</a>
    语法支持，类似于
    <a href="/language/types/string.html#language.types.string.syntax.heredoc" class="link">Heredoc</a>
    语法，但是包含单引号。 </span>
-   <span class="simpara"> 使用
    <a href="/language/types/string.html#language.types.string.syntax.heredoc" class="link">Heredoc</a>
    来初始化静态变量和类属性/常量变为可能。 </span>
-   <span class="simpara"> 可使用双引号声明
    <a href="/language/types/string.html#language.types.string.syntax.heredoc" class="link">Heredoc</a>，补充了
    <a href="/language/types/string.html#language.types.string.syntax.nowdoc" class="link">Nowdoc</a>
    语法。 </span>
-   <span class="simpara"> 可在类外部使用 *const* 关键词声明
    <a href="/language/constants/syntax.html" class="link">常量</a>。
    </span>
-   <span class="simpara">
    <a href="/language/operators/comparison.html#language.operators.comparison.ternary" class="link">三元运算</a>
    操作符有了简写形式：*?:*。 </span>
-   <span class="simpara"> HTTP 流包裹器将从 200 到 399
    全部的状态码都视为成功。 </span>
-   <span class="simpara"> 动态访问静态方法变为可能。 </span>
    ``` php
    <?php
    class C {
       public static $foo = 123;
    }

    $a = "C";
    echo $a::$foo;
    ?>
    ```

    以上例程会输出：

        123
-   <span class="simpara">
    <a href="/language/exceptions.html" class="link">异常</a>可以被内嵌：
    </span>
    ``` php
    <?php
    class MyCustomException extends Exception {}

    try {
        throw new MyCustomException("Exceptional", 112);
    } catch (Exception $e) {
        /* Note the use of the third parameter to pass $e
         * into the RuntimeException. */
        throw new RuntimeException("Rethrowing", 911, $e);
    }
    ?>
    ```
-   <span class="simpara"> 新增了循环引用的
    <a href="/features/gc.html" class="link">垃圾回收器</a>
    并且默认是开启的。 </span>
-   <span class="simpara"> <span class="function">mail</span>
    现在支持邮件发送日志，需要通过
    <a href="/mail/setup.html#" class="link">mail.log</a> 配置。(注意:
    仅支持通过该函数发送的邮件)。 </span>
