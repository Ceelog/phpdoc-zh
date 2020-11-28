expect\_expectl
===============

Waits until the output from a process matches one of the patterns, a
specified time period has passed, or an EOF is seen

### 说明

<span class="type">int</span> <span
class="methodname">expect\_expectl</span> ( <span
class="methodparam"><span class="type">resource</span> `$expect`</span>
, <span class="methodparam"><span class="type">array</span>
`$cases`</span> \[, <span class="methodparam"><span
class="type">array</span> `&$match`</span> \] )

Waits until the output from a process matches one of the patterns, a
specified time period has passed, or an EOF is seen.

If `match` is provided, then it is filled with the result of search. The
matched string can be found in `match[0]`. The match substrings
(according to the parentheses) in the original pattern can be found in
`match[1]`, `match[2]`, and so on, up to `match[9]` (the limitation of
libexpect).

### 参数

`expect`  
An Expect stream, previously opened with <span
class="function">expect\_popen</span>.

`cases`  
An array of expect cases. Each expect case is an indexed array, as
described in the following table:

| Index Key | Value Type | Description                                                                                                                                                                                                                                                                                                | Is Mandatory | Default Value                                                                             |
|-----------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|-------------------------------------------------------------------------------------------|
| 0         | string     | pattern, that will be matched against the output from the stream                                                                                                                                                                                                                                           | yes          |                                                                                           |
| 1         | mixed      | value, that will be returned by this function, if the pattern matches                                                                                                                                                                                                                                      | yes          |                                                                                           |
| 2         | integer    | pattern type, one of: <a href="/expect/constants.html#" class="link"><strong><code>EXP_GLOB</code></strong></a>, <a href="/expect/constants.html#" class="link"><strong><code>EXP_EXACT</code></strong></a> or <a href="/expect/constants.html#" class="link"><strong><code>EXP_REGEXP</code></strong></a> | no           | <a href="/expect/constants.html#" class="link"><strong><code>EXP_GLOB</code></strong></a> |

### 返回值

Returns value associated with the pattern that was matched.

On failure this function returns:
<a href="/expect/constants.html#" class="link"><strong><code>EXP_EOF</code></strong></a>,
<a href="/expect/constants.html#" class="link"><strong><code>EXP_TIMEOUT</code></strong></a>
or
<a href="/expect/constants.html#" class="link"><strong><code>EXP_FULLBUFFER</code></strong></a>

### 更新日志

| 版本              | 说明                                                                                                        |
|-------------------|-------------------------------------------------------------------------------------------------------------|
| PECL expect 0.2.1 | Prior to version 0.2.1, in `match` parameter a match string was returned, not an array of match substrings. |

### 范例

**示例 \#1 <span class="function">expect\_expectl</span> example**

``` php
<?php
// Copies file from remote host:
ini_set("expect.timeout", 30);

$stream = fopen("expect://scp user@remotehost:/var/log/messages /home/user/messages.txt", "r");

$cases = array(
    // array(pattern, value to return if pattern matched)
    array("password:", "asked for password"),
    array("yes/no)?",  "asked for yes/no")
);

while (true) {
    switch (expect_expectl($stream, $cases)) {
        case "asked for password":
            fwrite($stream, "my password\n");
            break;
        case "asked for yes/no":
            fwrite($stream, "yes\n");
            break;
        case EXP_TIMEOUT:
        case EXP_EOF:
            break 2; // break both the switch statement and the while loop
        default:
            die "Error has occurred!";
    }
}

fclose($stream);
?>
```

### 参见

-   <span class="function">expect\_popen</span>

expect\_popen
=============

Execute command via Bourne shell, and open the PTY stream to the process

### 说明

<span class="type"><span class="type">resource</span><span
class="type">false</span></span> <span
class="methodname">expect\_popen</span> ( <span
class="methodparam"><span class="type">string</span> `$command`</span> )

Execute command via Bourne shell, and open the PTY stream to the
process.

### 参数

`command`  
Command to execute.

### 返回值

Returns an open PTY stream to the processes *stdio*, *stdout*, and
*stderr*.

On failure this function returns **`FALSE`**.

### 范例

**示例 \#1 <span class="function">expect\_popen</span> example**

``` php
<?php
// Login to the PHP.net CVS repository:
$stream = expect_popen ("cvs -d :pserver:anonymous@cvs.php.net:/repository login");
sleep (3);
fwrite ($stream, "phpfi\n");
fclose ($stream);
?>
```

### 参见

-   <span class="function">popen</span>

**目录**

-   [expect\_expectl](/ref/expect.html#expect_expectl) — Waits until the
    output from a process matches one of the patterns, a specified time
    period has passed, or an EOF is seen
-   [expect\_popen](/ref/expect.html#expect_popen) — Execute command via
    Bourne shell, and open the PTY stream to the process
