password\_algos
===============

Get available password hashing algorithm IDs

### 说明

<span class="type">array</span> <span
class="methodname">password\_algos</span> ( <span
class="methodparam">void</span> )

Returns a complete list of all registered password hashing algorithm IDs
as an <span class="type">array</span> of <span
class="type">string</span>s.

### 参数

此函数没有参数。

### 返回值

Returns the available password hashing algorithm IDs.

### 范例

**示例 \#1 Basic <span class="function">password</span> usage**

``` php
<?php
print_r(password_algos());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 2y
        [1] => argon2i
        [2] => argon2id
    )

password\_get\_info
===================

返回指定散列（hash）的相关信息

### 说明

<span class="type">array</span> <span
class="methodname">password\_get\_info</span> ( <span
class="methodparam"><span class="type">string</span> `$hash`</span> )

如果传入的散列值（hash）是由 <span
class="function">password\_hash</span> 支持的算法生成的，
这个函数就会返回关于此散列的信息数组。

### 参数

`hash`  
一个由 <span class="function">password\_hash</span> 创建的散列值。

### 返回值

返回三个元素的关联数组：

-   <span class="simpara"> *algo*， 匹配
    <a href="/password/constants.html" class="link">密码算法的常量</a>
    </span>
-   <span class="simpara"> *algoName*，人类可读的算法名称 </span>
-   <span class="simpara"> *options*，调用 <span
    class="function">password\_hash</span> 时提供的选项。 </span>

password\_hash
==============

创建密码的散列（hash）

### 说明

<span class="type">string</span> <span
class="methodname">password\_hash</span> ( <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">int</span> `$algo`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

<span class="function">password\_hash</span>
使用足够强度的单向散列算法创建密码的散列（hash）。 <span
class="function">password\_hash</span> 兼容 <span
class="function">crypt</span>。 所以， <span
class="function">crypt</span> 创建的密码散列也可用于 <span
class="function">password\_hash</span>。

当前支持的算法：

-   <span class="simpara"> **`PASSWORD_DEFAULT`** - 使用 bcrypt 算法
    (PHP 5.5.0 默认)。 注意，该常量会随着 PHP
    加入更新更高强度的算法而改变。
    所以，使用此常量生成结果的长度将在未来有变化。
    因此，数据库里储存结果的列可超过60个字符（最好是255个字符）。
    </span>
-   <span class="simpara"> **`PASSWORD_BCRYPT`** - 使用
    **`CRYPT_BLOWFISH`** 算法创建散列。 这会产生兼容使用 "$2y$" 的 <span
    class="function">crypt</span>。 结果将会是 60 个字符的字符串，
    或者在失败时返回 **`FALSE`**。 </span>
-   <span class="simpara"> **`PASSWORD_ARGON2I`** - 使用 Argon2
    散列算法创建散列。 </span>

**`PASSWORD_BCRYPT`** 支持的选项：

-   *salt*(<span class="type">string</span>) -
    手动提供散列密码的盐值（salt）。这将避免自动生成盐值（salt）。

    省略此值后，<span class="function">password\_hash</span>
    会为每个密码散列自动生成随机的盐值。这种操作是有意的模式。

    **Warning**
    盐值（salt）选项从 PHP 7.0.0 开始被废弃（deprecated）了。
    现在最好选择简单的使用默认产生的盐值。

-   *cost* (<span class="type">integer</span>) - 代表算法使用的
    cost。<span class="function">crypt</span> 页面上有 cost 值的例子。

    省略时，默认值是 *10*。 这个 cost
    是个不错的底线，但也许可以根据自己硬件的情况，加大这个值。

**`PASSWORD_ARGON2I`** 支持的选项：

-   *memory\_cost* (<span class="type">integer</span>) - 计算 Argon2
    散列时的最大内存（单位：字节 byte）。默认值：
    **`PASSWORD_ARGON2_DEFAULT_MEMORY_COST`**。

-   *time\_cost* (<span class="type">integer</span>) - 计算 Argon2
    散列时最多的时间。默认值： **`PASSWORD_ARGON2_DEFAULT_TIME_COST`**。

-   *threads* (<span class="type">integer</span>) - 计算 Argon2
    散列时最多的线程数。默认值： **`PASSWORD_ARGON2_DEFAULT_THREADS`**。

### 参数

`password`  
用户的密码。

**Caution**
使用**`PASSWORD_BCRYPT`** 做算法，将使 `password`
参数最长为72个字符，超过会被截断。

`algo`  
一个用来在散列密码时指示算法的<a href="/password/constants.html" class="link">密码算法常量</a>。

`options`  
一个包含有选项的关联数组。目前支持两个选项：*salt*，在散列密码时加的盐（干扰字符串），以及*cost*，用来指明算法递归的层数。这两个值的例子可在
<span class="function">crypt</span> 页面找到。

省略后，将使用随机盐值与默认 cost。

### 返回值

返回散列后的密码， 或者在失败时返回 **`FALSE`**。

使用的算法、cost
和盐值作为散列的一部分返回。所以验证散列值的所有信息都已经包含在内。
这使 <span class="function">password\_verify</span>
函数验证的时候，不需要额外储存盐值或者算法的信息。

### 范例

**示例 \#1 <span class="function">password\_hash</span> 例子**

``` php
<?php
/**
 * 我们想要使用默认算法散列密码
 * 当前是 BCRYPT，并会产生 60 个字符的结果。
 *
 * 请注意，随时间推移，默认算法可能会有变化，
 * 所以需要储存的空间能够超过 60 字（255字不错）
 */
echo password_hash("rasmuslerdorf", PASSWORD_DEFAULT);
?>
```

以上例程的输出类似于：

    $2y$10$.vGA1O9wmRjrwAVXD98HNOgsNpDczlqm3Jq7KnEd1rVAGv3Fykk1a

**示例 \#2 <span class="function">password\_hash</span> 手动设置 cost
的例子**

``` php
<?php
/**
 * 在这个案例里，我们为 BCRYPT 增加 cost 到 12。
 * 注意，我们已经切换到了，将始终产生 60 个字符。
 */
$options = [
    'cost' => 12,
];
echo password_hash("rasmuslerdorf", PASSWORD_BCRYPT, $options);
?>
```

以上例程的输出类似于：

    $2y$12$QjSH496pcT5CEbzjD/vtVeH03tfHKFy36d4J0Ltp3lRtee9HDxY3K

**示例 \#3 <span class="function">password\_hash</span>
手动设置盐值的例子**

``` php
<?php
/**
 * 注意，这里的盐值是随机产生的。
 * 永远都不要使用固定盐值，或者不是随机生成的盐值。
 *
 * 绝大多数情况下，可以让 password_hash generate 为你自动产生随机盐值
 */
$options = [
    'cost' => 11,
    'salt' => mcrypt_create_iv(22, MCRYPT_DEV_URANDOM),
];
echo password_hash("rasmuslerdorf", PASSWORD_BCRYPT, $options);
?>
```

以上例程的输出类似于：

    $2y$11$q5MkhSBtlsJcNEVsYh64a.aCluzHnGog7TQAKVmQwO9C8xb.t89F.

**示例 \#4 寻找最佳 cost 的 <span class="function">password\_hash</span>
例子**

``` php
<?php
/**
 * 这个例子对服务器做了基准测试（benchmark），检测服务器能承受多高的 cost
 * 在不明显拖慢服务器的情况下可以设置最高的值
 * 8-10 是个不错的底线，在服务器够快的情况下，越高越好。
 * 以下代码目标为  ≤ 50 毫秒（milliseconds），
 * 适合系统处理交互登录。
 */
$timeTarget = 0.05; // 50 毫秒（milliseconds） 

$cost = 8;
do {
    $cost++;
    $start = microtime(true);
    password_hash("test", PASSWORD_BCRYPT, ["cost" => $cost]);
    $end = microtime(true);
} while (($end - $start) < $timeTarget);

echo "Appropriate Cost Found: " . $cost;
?>
```

以上例程的输出类似于：

    Appropriate Cost Found: 10

**示例 \#5 使用 Argon2 的<span
class="function">password\_hash</span>例子**

``` php
<?php
echo 'Argon2 hash: ' . password_hash('rasmuslerdorf', PASSWORD_ARGON2I);
?>
```

以上例程的输出类似于：

    Argon2 hash: $argon2i$v=19$m=1024,t=2,p=2$YzJBSzV4TUhkMzc3d3laeg$zqU/1IN0/AogfP4cmSJI1vc8lpXRW9/S0sYY2i2jHT0

### 注释

**Caution**

强烈建议不要自己为这个函数生成盐值（salt）。只要不设置，它会自动创建安全的盐值。

就像以上提及的，在 PHP 7.0 提供
*salt*选项会导致废弃（deprecation）警告。 未来的 PHP
发行版里，手动提供盐值的功能可能会被删掉。

> **Note**:
>
> 在交互的系统上，推荐在自己的服务器上测试此函数，调整 cost
> 参数直至函数时间开销小于 100 毫秒（milliseconds）。
> 上面脚本的例子会帮助选择合适硬件的最佳 cost。

> **Note**: <span class="simpara">
> 这个函数更新支持的算法时（或修改默认算法），必定会遵守以下规则：
> </span>
>
> -   <span class="simpara"> 任何内核中的新算法必须在经历一次 PHP
>     完整发行才能成为默认算法。 比如，在 PHP 7.5.5 中添加的新算法，在
>     PHP 7.7 之前不能成为默认算法 （由于 7.6 是第一个完整发行版）。
>     但如果是在 7.6.0 里添加的不同算法，在 7.7.0 里也可以成为默认算法。
>     </span>
> -   <span class="simpara"> 仅仅允许在完整发行版中修改默认算法（比如
>     7.3.0, 8.0.0，等等），不能是在修订版。
>     唯一的例外是：在当前默认算法里发现了紧急的安全威胁。 </span>

### 更新日志

| 版本  | 说明                                                    |
|-------|---------------------------------------------------------|
| 7.2.0 | 添加 **`PASSWORD_ARGON2I`**，支持 Argon2 密码散列算法。 |

### 参见

-   <span class="function">password\_verify</span>
-   <span class="function">crypt</span>
-   <a href="https://github.com/ircmaxell/password_compat" class="link external">» 用户的使用</a>

password\_needs\_rehash
=======================

检测散列值是否匹配指定的选项

### 说明

<span class="type">bool</span> <span
class="methodname">password\_needs\_rehash</span> ( <span
class="methodparam"><span class="type">string</span> `$hash`</span> ,
<span class="methodparam"><span class="type">int</span> `$algo`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$options`</span> \] )

此函数检测指定的散列值是否实现了提供的算法和选项。
如果没有，需要重新生成散列值。

### 参数

`hash`  
一个由 <span class="function">password\_hash</span> 创建的散列值。

`algo`  
一个用来在散列密码时指示算法的<a href="/password/constants.html" class="link">密码算法常量</a>。

`options`  
一个包含有选项的关联数组。目前支持两个选项：*salt*，在散列密码时加的盐（干扰字符串），以及*cost*，用来指明算法递归的层数。这两个值的例子可在
<span class="function">crypt</span> 页面找到。

### 范例

**示例 \#1 <span class="function">password\_needs\_rehash</span>用法**

``` php
<?php

$password = 'rasmuslerdorf';
$hash = '$2y$10$YCFsG6elYca568hBi2pZ0.3LDL5wjgxct1N8w/oLR/jfHsiQwCqTS';

// 当硬件性能得到改善时，cost 参数可以再修改
$options = array('cost' => 11);

// 根据明文密码验证储存的散列
if (password_verify($password, $hash)) {
    // 检测是否有更新的可用散列算法
    // 或者 cost 发生变化
    if (password_needs_rehash($hash, PASSWORD_DEFAULT, $options)) {
        // 如果是这样，则创建新散列，替换旧散列
        $newHash = password_hash($password, PASSWORD_DEFAULT, $options);
    }

    // 使用户登录
}
?>
```

### 返回值

如果散列需要重新生成才能匹配指定的 `algo` 和 `options`， 则返回
**`TRUE`**，否则返回 **`FALSE`**。

password\_verify
================

验证密码是否和散列值匹配

### 说明

<span class="type">bool</span> <span
class="methodname">password\_verify</span> ( <span
class="methodparam"><span class="type">string</span> `$password`</span>
, <span class="methodparam"><span class="type">string</span>
`$hash`</span> )

验证密码是否和指定的散列值匹配。

注意 <span class="function">password\_hash</span> 返回的散列包含了算法、
cost 和盐值。
因此，所有需要的信息都包含内。使得验证函数不需要储存额外盐值等信息即可验证哈希。

时序攻击（timing attacks）对此函数不起作用。

### 参数

`password`  
用户的密码。

`hash`  
一个由 <span class="function">password\_hash</span> 创建的散列值。

### 返回值

如果密码和散列值匹配则返回 **`TRUE`**，否则返回 **`FALSE`** 。

### 范例

**示例 \#1 <span class="function">password\_verify</span> 例子**

``` php
<?php
// 想知道以下字符从哪里来，可参见 password_hash() 的例子
$hash = '$2y$07$BCryptRequires22Chrcte/VlQH0piJtjXl.0t1XkA8pw9dMXTpOq';

if (password_verify('rasmuslerdorf', $hash)) {
    echo 'Password is valid!';
} else {
    echo 'Invalid password.';
}
?>
```

以上例程会输出：

    Password is valid!

### 参见

-   <span class="function">password\_hash</span>
-   <a href="https://github.com/ircmaxell/password_compat" class="link external">» 用户使用</a>

**目录**

-   [password\_algos](/ref/password.html#password_algos) — Get available
    password hashing algorithm IDs
-   [password\_get\_info](/ref/password.html#password_get_info) —
    返回指定散列（hash）的相关信息
-   [password\_hash](/ref/password.html#password_hash) —
    创建密码的散列（hash）
-   [password\_needs\_rehash](/ref/password.html#password_needs_rehash)
    — 检测散列值是否匹配指定的选项
-   [password\_verify](/ref/password.html#password_verify) —
    验证密码是否和散列值匹配
