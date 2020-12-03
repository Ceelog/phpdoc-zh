*match*
-------

The *match* expression branches evaluation based on an identity check of
a value. Similarly to a *switch* statement, a *match* expression has a
subject expression that is compared against multiple alternatives.
Unlike *switch*, it will evaluate to a value much like ternary
expressions. Unlike *switch*, the comparison is an identity check
(`===`) rather than a weak equality check (`==`). Match expressions are
available as of PHP 8.0.0.

**示例 \#1 Structure of a *match* expression**

``` php
<?php
$return_value = match (subject_expression) {
    single_conditional_expression => return_expression,
    conditional_expression1, conditional_expression2 => return_expression,
};
?>
```

> **Note**: <span class="simpara"> The result of a *match* expression
> does not need to be used. </span>

> **Note**: <span class="simpara"> A *match* expression *must* be
> terminated by a semicolon *;*. </span>

The *match* expression is similar to a *switch* statement but has some
key differences:

-   <span class="simpara"> A *match* arm compares values strictly
    (`===`) instead of loosely as the switch statement does. </span>
-   <span class="simpara"> A *match* expression returns a value. </span>
-   <span class="simpara"> *Match* arms do not fall-through to later
    cases the way *switch* statements do. </span>
-   <span class="simpara"> A *match* expression must be exhaustive.
    </span>

As *switch* statements, *match* expressions are executed match arm by
match arm. In the beginning, no code is executed. The conditional
expressions are only evaluated if all previous conditional expressions
failed to match the subject expression. Only the return expression
corresponding to the matching conditional expression will be evaluated.
For example:

``` php
<?php
$result = match ($x) {
    foo() => ...,
    $this->bar() => ..., // bar() isn't called if foo() === $x
    $this->baz => beep(), // beep() isn't called unless $x === $this->baz
    // etc.
};
?>
```

*match* expression arms may contain multiple expressions separated by a
comma. That is a logical OR, and is a short-hand for multiple match arms
with the same right-hand side.

``` php
<?php
$result = match ($x) {
    // This match arm:
    $a, $b, $c => 5,
    // Is equivalent to these three match arms:
    $a => 5,
    $b => 5,
    $c => 5,
};
?>
```

A special case is the *default* pattern. This pattern matches anything
that wasn't previously matched. For example:

``` php
<?php
$expressionResult = match ($condition) {
    1, 2 => foo(),
    3, 4 => bar(),
    default => baz(),
};
?>
```

> **Note**: <span class="simpara"> Multiple default patterns will raise
> a **`E_FATAL_ERROR`** error. </span>

A *match* expression must be exhaustive. If the subject expression is
not handled by any match arm an <span
class="classname">UnhandledMatchError</span> is thrown.

**示例 \#2 Example of an unhandled match expression**

``` php
<?php
$condition = 5;

try {
    match ($condition) {
        1, 2 => foo(),
        3, 4 => bar(),
    };
} catch (\UnhandledMatchError $e) {
    var_dump($e);
}
?>
```

以上例程会输出：

    object(UnhandledMatchError)#1 (7) {
      ["message":protected]=>
      string(33) "Unhandled match value of type int"
      ["string":"Error":private]=>
      string(0) ""
      ["code":protected]=>
      int(0)
      ["file":protected]=>
      string(9) "/in/ICgGK"
      ["line":protected]=>
      int(6)
      ["trace":"Error":private]=>
      array(0) {
      }
      ["previous":"Error":private]=>
      NULL
    }

### Using match expressions to handle non identity checks

It is possible to use a *match* expression to handle non-identity
conditional cases by using `true` as the subject expression.

**示例 \#3 Using a generalized match expressions to branch on integer
ranges**

``` php
<?php

$age = 23;

$result = match (true) {
    $age >= 65 => 'senior',
    $age >= 25 => 'adult',
    $age >= 18 => 'young adult',
    default => 'kid',
};

var_dump($result);
?>
```

以上例程会输出：

    string(11) "young adult"

**示例 \#4 Using a generalized match expressions to branch on string
content**

``` php
<?php

$text = 'Bienvenue chez nous';

$result = match (true) {
    str_contains($text, 'Welcome') || str_contains($text, 'Hello') => 'en',
    str_contains($text, 'Bienvenue') || str_contains($text, 'Bonjour') => 'fr',
    // ...
};

var_dump($result);
?>
```

以上例程会输出：

    string(2) "fr"
