Taint is an extension, which is used for detecting XSS codes(tainted
string). And also can be used to spot sql injection vulnerabilities, and
shell inject, etc.

When taint is enabled, if you pass a tainted string (comes from $\_GET,
$\_POST or $\_COOKIE) to some functions, taint will warn you about that.

**示例 \#1 <span class="function">Taint</span>example**

``` php
<?php
$a = trim($_GET['a']);

$file_name = '/tmp' .  $a;
$output    = "Welcome, {$a} !!!";
$var       = "output";
$sql       = "Select *  from " . $a;
$sql      .= "ooxx";

echo $output;

print $$var;

include($file_name);

mysql_query($sql);
?>
```

以上例程的输出类似于：

    Warning: main() [function.echo]: Attempt to echo a string that might be tainted

    Warning: main() [function.echo]: Attempt to print a string that might be tainted

    Warning: include() [function.include]: File path contains data that might be tainted

    Warning: mysql_query() [function.mysql-query]: SQL statement contains data that might be tainted
