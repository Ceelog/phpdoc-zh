新特性
------

### PHP 核心中的新特性

#### 命名参数

#### 注解（Attributes）

新增注解的功能。

#### 构造器属性提升（Constructor Property Promotion）

新增构造器属性提升功能（在构造函数中声明类的属性）。

#### 联合类型

新增
<a href="/language/types/declarations.html#language.types.declarations.union" class="link">联合类型</a>。

#### Match 表达式

新增
<a href="/control-structures/match.html" class="link"><em>match</em> 表达式</a>。

#### Nullsafe 运算符

新增 Nullsafe 运算符(*?-\>*)。

#### 其他新特性

-   新增 *WeakMap* 类。

-   新增 <span class="classname">ValueError</span> 类。

-   现在，只要类型兼容，任意数量的函数参数都可以用一个可变参数替换。
    例如允许编写下面的代码：

    ``` php
    <?php
    class A {
         public function method(int $many, string $parameters, $here) {}
    }
    class B extends A {
         public function method(...$everything) {}
    }
    ?>
    ```

-   <span class="type">static</span> ("后期静态绑定"中)
    可以作为返回类型：

    ``` php
    <?php
    class Test {
         public function create(): static {
              return new static();
         }
    }
    ?>
    ```

-   现在可以通过 `$object::class` 获取类名，返回的结果和
    `get_class($object)` 一致。

-   <a href="/language/oop5/basic.html#language.oop5.basic.new" class="link"><em>new</em></a>、<a href="/language/operators/type.html" class="link"><em>instanceof</em></a>
    可用于任何表达式， 用法为 `new (expression)(...$args)` 和
    `$obj instanceof (expression)`。

-   添加对一些变量语法一致性的修复，例如现在能够编写 `Foo::BAR::$baz`。

-   添加 <span class="interfacename">Stringable</span> interface，
    当一个类定义
    <a href="/language/oop5/magic.html#object.tostring" class="link">__toString()</a>
    方法后会自动实现该接口。

-   Trait 可以定义私有抽象方法（abstract private method）。 类必须实现
    trait 定义的该方法。

-   可作为表达式使用 *throw*。 使得可以编写以下用法：

    ``` php
    <?php
    $fn = fn() => throw new Exception('Exception in arrow function');
    $user = $session->user ?? throw new Exception('Must have user');
    ```

-   参数列表中的末尾逗号为可选。

    ``` php
    <?php
    function functionWithLongSignature(
        Type1 $parameter1,
        Type2 $parameter2, // <-- 这个逗号也被允许了
    ) {
    }
    ```

-   现在允许 `catch (Exception)` 一个 exception 而无需捕获到变量中。

-   支持 <span class="type">mixed</span> 类型。

-   Private methods declared on a parent class no longer enforce any
    inheritance rules on the methods of a child class (with the
    exception of final private constructors). The following example
    illustrates which restrictions have been removed:

    ``` php
    <?php
    class ParentClass {
        private function method1() {}
        private function method2() {}
        private static function method3() {}
        // Throws a warning, as "final" no longer has an effect:
        private final function method4() {}
    }
    class ChildClass extends ParentClass {
        // All of the following are now allowed, even though the modifiers aren't
        // the same as for the private methods in the parent class.
        public abstract function method1() {}
        public static function method2() {}
        public function method3() {}
        public function method4() {}
    }
    ?>
    ```

-   <span class="function">get\_resource\_id</span> has been added,
    which returns the same value as `(int) $resource`. It provides the
    same functionality under a clearer API.

### Date and Time

-   <span class="methodname">DateTime::createFromInterface</span> and
    <span
    class="methodname">DateTimeImmutable::createFromInterface</span>
    have been added.

-   The DateTime format specifier *p* has been added, which is the same
    as *P* but returns *Z* rather than *+00:00* for UTC.

### DOM

<span class="interfacename">DOMParentNode</span> and <span
class="interfacename">DOMChildNode</span> with new traversal and
manipulation APIs have been added.

### Filter

**`FILTER_VALIDATE_BOOL`** has been added as an alias for
**`FILTER_VALIDATE_BOOLEAN`**. The new name is preferred, as it uses the
canonical type name.

### Enchant

<span class="function">enchant\_dict\_add</span>, <span
class="function">enchant\_dict\_is\_added</span>, and
**`LIBENCHANT_VERSION`** have been added.

### FPM

Added a new option *pm.status\_listen* that allows getting the status
from different endpoint (e.g. port or UDS file) which is useful for
getting the status when all children are busy with serving long running
requests.

### Hash

<span class="classname">HashContext</span> objects can now be
serialized.

### Internationalization Functions

The **`IntlDateFormatter::RELATIVE_FULL`**,
**`IntlDateFormatter::RELATIVE_LONG`**,
**`IntlDateFormatter::RELATIVE_MEDIUM`**, and
**`IntlDateFormatter::RELATIVE_SHORT`** constants have been added.

### LDAP

<span class="function">ldap\_count\_references</span> has been added,
which returns the number of reference messages in a search result.

### OPcache

If the opcache.record\_warnings ini setting is enabled, OPcache will
record compile-time warnings and replay them on the next include, even
if it is served from cache.

### OpenSSL

Added Cryptographic Message Syntax (CMS)
(<a href="http://www.faqs.org/rfcs/rfc5652" class="link external">» RFC 5652</a>)
support composed of functions for encryption, decryption, signing,
verifying and reading. The API is similar to the API for PKCS \#7
functions with an addition of new encoding constants:
**`OPENSSL_ENCODING_DER`**, **`OPENSSL_ENCODING_SMIME`** and
**`OPENSSL_ENCODING_PEM`**:

-   <span class="function">openssl\_cms\_encrypt</span> encrypts the
    message in the file with the certificates and outputs the result to
    the supplied file.
-   <span class="function">openssl\_cms\_decrypt</span> that decrypts
    the S/MIME message in the file and outputs the results to the
    supplied file.
-   <span class="function">openssl\_cms\_read</span> that exports the
    CMS file to an array of PEM certificates.
-   <span class="function">openssl\_cms\_sign</span> that signs the MIME
    message in the file with a cert and key and output the result to the
    supplied file.
-   <span class="function">openssl\_cms\_verify</span> that verifies
    that the data block is intact, the signer is who they say they are,
    and returns the certs of the signers.

### Regular Expressions (Perl-Compatible)

<span class="function">preg\_last\_error\_msg</span> has been added,
which returns a human-readable message for the last PCRE error. It
complements <span class="function">preg\_last\_error</span>, which
returns an integer enum value instead.

### Reflection

-   The following methods can now return information about default
    values of parameters of internal functions:

    -   <span
        class="methodname">ReflectionParameter::isDefaultValueAvailable</span>
    -   <span
        class="methodname">ReflectionParameter::getDefaultValue</span>
    -   <span
        class="methodname">ReflectionParameter::isDefaultValueConstant</span>
    -   <span
        class="methodname">ReflectionParameter::getDefaultValueConstantName</span>

### SQLite3

<span class="methodname">SQLite3::setAuthorizer</span> and respective
class constants have been added to set a userland callback that will be
used to authorize or not an action on the database.

### Standard Library

-   <span class="function">str\_contains</span>, <span
    class="function">str\_starts\_with</span> and <span
    class="function">str\_ends\_with</span> have been added, which check
    whether `haystack` contains, starts with or ends with `needle`,
    respectively.

-   <span class="function">fdiv</span> has been added, which performs a
    floating-point division under IEEE 754 semantics. Division by zero
    is considered well-defined and will return one of *Inf*, *-Inf* or
    *NaN*.

-   <span class="function">get\_debug\_type</span> has been added, which
    returns a type useful for error messages. Unlike <span
    class="function">gettype</span>, it uses canonical type names,
    returns class names for objects, and indicates the resource type for
    resources.

-   <span class="function">printf</span> and friends now support the
    *%h* and *%H* format specifiers. These are the same as *%g* and
    *%G*, but always use *"."* as the decimal separator, rather than
    determining it through the **`LC_NUMERIC`** locale.

-   <span class="function">printf</span> and friends now support using
    *"\*"* as width or precision, in which case the width/precision is
    passed as an argument to printf. This also allows using precision
    *-1* with *%g*, *%G*, *%h* and *%H*. For example, the following code
    can be used to reproduce PHP's default floating point formatting:

    ``` php
    <?php
    printf("%.*H", (int) ini_get("precision"), $float);
    printf("%.*H", (int) ini_get("serialize_precision"), $float);
    ?>
    ```

-   <span class="function">proc\_open</span> now supports
    pseudo-terminal (PTY) descriptors. The following attaches *stdin*,
    *stdout* and *stderr* to the same PTY:

    ``` php
    <?php
    $proc = proc_open($command, [['pty'], ['pty'], ['pty']], $pipes);
    ?>
    ```

-   <span class="function">proc\_open</span> now supports socket pair
    descriptors. The following attaches a distinct socket pair to
    *stdin*, *stdout* and *stderr*:

    ``` php
    <?php
    $proc = proc_open($command, [['socket'], ['socket'], ['socket']], $pipes);
    ?>
    ```

    Unlike pipes, sockets do not suffer from blocking I/O issues on
    Windows. However, not all programs may work correctly with stdio
    sockets.

-   Sorting functions are now stable, which means that equal-comparing
    elements will retain their original order.

-   <span class="function">array\_diff</span>, <span
    class="function">array\_intersect</span> and their variations can
    now be used with a single array as argument. This means that usages
    like the following are now possible:

    ``` php
    <?php
    // OK even if $excludes is empty:
    array_diff($array, ...$excludes);
    // OK even if $arrays only contains a single array:
    array_intersect(...$arrays);
    ?>
    ```

-   The `flag` parameter of <span
    class="function">ob\_implicit\_flush</span> was changed to accept a
    <span class="type">bool</span> rather than an <span
    class="type">int</span>.

### Tokenizer

<span class="classname">PhpToken</span> adds an object-based interface
to the tokenizer. It provides a more uniform and ergonomic
representation, while being more memory efficient and faster.

### Zip

-   The Zip extension has been updated to version 1.19.1.

-   New <span class="methodname">ZipArchive::setMtimeName</span> and
    <span class="methodname">ZipArchive::setMtimeIndex</span> to set the
    modification time of an entry.

-   New <span
    class="methodname">ZipArchive::registerProgressCallback</span> to
    provide updates during archive close.

-   New <span
    class="methodname">ZipArchive::registerCancelCallback</span> to
    allow cancellation during archive close.

-   New <span class="methodname">ZipArchive::replaceFile</span> to
    replace an entry content.

-   New <span
    class="methodname">ZipArchive::isCompressionMethodSupported</span>
    to check optional compression features.

-   New <span
    class="methodname">ZipArchive::isEncryptionMethodSupported</span> to
    check optional encryption features.

-   The `ZipArchive::lastId` property to get the index value of the last
    added entry has been added.

-   Errors can now be checked after an archive has been closed using the
    `ZipArchive::status` and `ZipArchive::statusSys` properties, or the
    <span class="methodname">ZipArchive::getStatusString</span> method.

-   The *'remove\_path'* option of <span
    class="methodname">ZipArchive::addGlob</span> and <span
    class="methodname">ZipArchive::addPattern</span> is now treated as
    an arbitrary string prefix (for consistency with the *'add\_path'*
    option), whereas formerly it was treated as a directory name.

-   Optional compression / encryption features are now listed in
    phpinfo.
