范例
====

**目录**

-   [Validation](/filter/examples.html#Validation)
-   [Sanitization](/filter/examples.html#Sanitization)

Validation
----------

**示例 \#1 Validating email addresses with <span
class="function">filter\_var</span>**

``` php
<?php
$email_a = 'joe@example.com';
$email_b = 'bogus';

if (filter_var($email_a, FILTER_VALIDATE_EMAIL)) {
    echo "Email address '$email_a' is considered valid.\n";
}
if (filter_var($email_b, FILTER_VALIDATE_EMAIL)) {
    echo "Email address '$email_b' is considered valid.\n";
} else {
    echo "Email address '$email_b' is considered invalid.\n";
}
?>
```

以上例程会输出：

    Email address 'joe@example.com' is considered valid.
    Email address 'bogus' is considered invalid.

**示例 \#2 Validating IP addresses with <span
class="function">filter\_var</span>**

``` php
<?php
$ip_a = '127.0.0.1';
$ip_b = '42.42';

if (filter_var($ip_a, FILTER_VALIDATE_IP)) {
    echo "IP address '$ip_a' is considered valid.";
}
if (filter_var($ip_b, FILTER_VALIDATE_IP)) {
    echo "IP address '$ip_b' is considered valid.";
}
?>
```

以上例程会输出：

    IP address '127.0.0.1' is considered valid.

**示例 \#3 Passing options to <span
class="function">filter\_var</span>**

``` php
<?php
$int_a = '1';
$int_b = '-1';
$int_c = '4';
$options = array(
    'options' => array(
        'min_range' => 0,
        'max_range' => 3,
    )
);
if (filter_var($int_a, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Integer A '$int_a' is considered valid (between 0 and 3).\n";
}
if (filter_var($int_b, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Integer B '$int_b' is considered valid (between 0 and 3).\n";
}
if (filter_var($int_c, FILTER_VALIDATE_INT, $options) !== FALSE) {
    echo "Integer C '$int_c' is considered valid (between 0 and 3).\n";
}

$options['options']['default'] = 1;
if (($int_c = filter_var($int_c, FILTER_VALIDATE_INT, $options)) !== FALSE) {
    echo "Integer C '$int_c' is considered valid (between 0 and 3).";
}
?>
```

以上例程会输出：

    Integer A '1' is considered valid (between 0 and 3).
    Integer C '1' is considered valid (between 0 and 3).

Sanitization
------------

**示例 \#1 Sanitizing and validating email addresses**

``` php
<?php
$a = 'joe@example.org';
$b = 'bogus - at - example dot org';
$c = '(bogus@example.org)';

$sanitized_a = filter_var($a, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_a, FILTER_VALIDATE_EMAIL)) {
    echo "This (a) sanitized email address is considered valid.\n";
}

$sanitized_b = filter_var($b, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_b, FILTER_VALIDATE_EMAIL)) {
    echo "This sanitized email address is considered valid.";
} else {
    echo "This (b) sanitized email address is considered invalid.\n";
}

$sanitized_c = filter_var($c, FILTER_SANITIZE_EMAIL);
if (filter_var($sanitized_c, FILTER_VALIDATE_EMAIL)) {
    echo "This (c) sanitized email address is considered valid.\n";
    echo "Before: $c\n";
    echo "After:  $sanitized_c\n";    
}
?>
```

以上例程会输出：

    This (a) sanitized email address is considered valid.
    This (b) sanitized email address is considered invalid.
    This (c) sanitized email address is considered valid.
    Before: (bogus@example.org)
    After: bogus@example.org

**示例 \#2 Configuring a default filter**

``` php
filter.default = full_special_chars
filter.default_flags = 0
```
