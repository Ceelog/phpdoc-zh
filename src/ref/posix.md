The section about
<a href="/book/pcntl.html" class="link">Process Control Functions</a>
maybe of interest for you.

posix\_access
=============

Determine accessibility of a file

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_access</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = POSIX\_F\_OK</span></span> \] )

<span class="function">posix\_access</span> checks the user's permission
of a file.

### 参数

`file`  
The name of the file to be tested.

`mode`  
A mask consisting of one or more of **`POSIX_F_OK`**, **`POSIX_R_OK`**,
**`POSIX_W_OK`** and **`POSIX_X_OK`**.

**`POSIX_R_OK`**, **`POSIX_W_OK`** and **`POSIX_X_OK`** request checking
whether the file exists and has read, write and execute permissions,
respectively. **`POSIX_F_OK`** just requests checking for the existence
of the file.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">posix\_access</span> example**

This example will check if the $file is readable and writable, otherwise
will print an error message.

``` php
<?php

$file = 'some_file';

if (posix_access($file, POSIX_R_OK | POSIX_W_OK)) {
    echo 'The file is readable and writable!';

} else {
    $error = posix_get_last_error();

    echo "Error $error: " . posix_strerror($error);
}

?>
```

### 注释

### 参见

-   <span class="function">posix\_get\_last\_error</span>
-   <span class="function">posix\_strerror</span>

posix\_ctermid
==============

Get path name of controlling terminal

### 说明

<span class="type">string</span> <span
class="methodname">posix\_ctermid</span> ( <span
class="methodparam">void</span> )

Generates a <span class="type">string</span> which is the pathname for
the current controlling terminal for the process. On error this will set
errno, which can be checked using <span
class="function">posix\_get\_last\_error</span>

### 返回值

Upon successful completion, returns <span class="type">string</span> of
the pathname to the current controlling terminal. Otherwise **`FALSE`**
is returned and errno is set, which can be checked with <span
class="function">posix\_get\_last\_error</span>.

### 范例

**示例 \#1 <span class="function">posix\_ctermid</span> example**

This example will display the path to the current TTY.

``` php
<?php
echo "I am running from ".posix_ctermid();
?>
```

### 参见

-   <span class="function">posix\_ttyname</span>
-   <span class="function">posix\_get\_last\_error</span>

posix\_errno
============

别名 <span class="function">posix\_get\_last\_error</span>

### 说明

此函数是该函数的别名： <span
class="function">posix\_get\_last\_error</span>.

posix\_get\_last\_error
=======================

Retrieve the error number set by the last posix function that failed

### 说明

<span class="type">int</span> <span
class="methodname">posix\_get\_last\_error</span> ( <span
class="methodparam">void</span> )

Retrieve the error number set by the last posix function that failed.
The system error message associated with the errno may be checked with
<span class="function">posix\_strerror</span>.

### 返回值

Returns the errno (error number) set by the last posix function that
failed. If no errors exist, 0 is returned.

### 范例

**示例 \#1 <span class="function">posix\_get\_last\_error</span>
example**

This example attempt to kill a bogus process id, which will set the last
error. We will then print out the last errno.

``` php
<?php
posix_kill(999459,SIGKILL);
echo 'Your error returned was '.posix_get_last_error(); //Your error was ___
?>
```

### 参见

-   <span class="function">posix\_strerror</span>

posix\_getcwd
=============

Pathname of current directory

### 说明

<span class="type">string</span> <span
class="methodname">posix\_getcwd</span> ( <span
class="methodparam">void</span> )

Gets the absolute pathname of the script's current working directory. On
error, it sets errno which can be checked using <span
class="function">posix\_get\_last\_error</span>

### 返回值

Returns a <span class="type">string</span> of the absolute pathname on
success. On error, returns **`FALSE`** and sets errno which can be
checked with <span class="function">posix\_get\_last\_error</span>.

### 范例

**示例 \#1 <span class="function">posix\_getcwd</span> example**

This example will return the absolute path of the current working
directory of the script.

``` php
<?php
echo 'My current working directory is '.posix_getcwd();
?>
```

### 注释

> **Note**:
>
> This function can fail on
>
> -   <span class="simpara">Read or Search permission was denied</span>
> -   <span class="simpara">Pathname no longer exists</span>

posix\_getegid
==============

Return the effective group ID of the current process

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getegid</span> ( <span
class="methodparam">void</span> )

Return the numeric effective group ID of the current process.

### 返回值

Returns an <span class="type">int</span> of the effective group ID.

### 范例

**示例 \#1 <span class="function">posix\_getegid</span> example**

This example will print out the effective group id, once it is changed
with <span class="function">posix\_setegid</span>.

``` php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### 注释

<span class="function">posix\_getegid</span> is different than <span
class="function">posix\_getgid</span> because effective group ID can be
changed by a calling process using <span
class="function">posix\_setegid</span>.

### 参见

-   <span class="function">posix\_getgrgid</span>
-   <span class="function">posix\_getgid</span>
-   <span class="function">posix\_setgid</span>

posix\_geteuid
==============

Return the effective user ID of the current process

### 说明

<span class="type">int</span> <span
class="methodname">posix\_geteuid</span> ( <span
class="methodparam">void</span> )

Return the numeric effective user ID of the current process. See also
<span class="function">posix\_getpwuid</span> for information on how to
convert this into a useable username.

### 返回值

Returns the user id, as an <span class="type">int</span>

### 范例

**示例 \#1 <span class="function">posix\_geteuid</span> example**

This example will show the current user id then set the effective user
id to a separate id using <span class="function">posix\_seteuid</span>,
then show the difference between the real id and the effective id.

``` php
<?php
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_seteuid(10000);
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10000
?>
```

### 参见

-   <span class="function">posix\_getpwuid</span>
-   <span class="function">posix\_getuid</span>
-   <span class="function">posix\_setuid</span>
-   POSIX man page GETEUID(2)

posix\_getgid
=============

Return the real group ID of the current process

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getgid</span> ( <span
class="methodparam">void</span> )

Return the numeric real group ID of the current process.

### 返回值

Returns the real group id, as an <span class="type">int</span>.

### 范例

**示例 \#1 <span class="function">posix\_getgid</span> example**

This example will print out the real group id, even once the effective
group id has been changed.

``` php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### 参见

-   <span class="function">posix\_getgrgid</span>
-   <span class="function">posix\_getegid</span>
-   <span class="function">posix\_setgid</span>
-   POSIX man page GETGID(2)

posix\_getgrgid
===============

Return info about a group by group id

### 说明

<span class="type">array</span> <span
class="methodname">posix\_getgrgid</span> ( <span
class="methodparam"><span class="type">int</span> `$gid`</span> )

Gets information about a group provided its id.

### 参数

`gid`  
The group id.

### 返回值

The array elements returned are:

| Element | Description                                                                                                                                                            |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name    | The name element contains the name of the group. This is a short, usually less than 16 character "handle" of the group, not the real, full name.                       |
| passwd  | The passwd element contains the group's password in an encrypted format. Often, for example on a system employing "shadow" passwords, an asterisk is returned instead. |
| gid     | Group ID, should be the same as the `gid` parameter used when calling the function, and hence redundant.                                                               |
| members | This consists of an <span class="type">array</span> of <span class="type">string</span>'s for all the members in the group.                                            |

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getgrgid</span>**

``` php
<?php

$groupid   = posix_getegid();
$groupinfo = posix_getgrgid($groupid);

print_r($groupinfo);
?>
```

以上例程的输出类似于：

    Array
    (
        [name]    => toons
        [passwd]  => x
        [members] => Array
            (
                [0] => tom
                [1] => jerry
            )
        [gid]     => 42
    )

### 参见

-   <span class="function">posix\_getegid</span>
-   <span class="function">posix\_getgrnam</span>
-   <span class="function">filegroup</span>
-   <span class="function">stat</span>
-   POSIX man page GETGRNAM(3)

posix\_getgrnam
===============

Return info about a group by name

### 说明

<span class="type"><span class="type">array</span><span
class="type">false</span></span> <span
class="methodname">posix\_getgrnam</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

Gets information about a group provided its name.

### 参数

`name`  
The name of the group

### 返回值

Returns an <span class="type">array</span> on success, 或者在失败时返回
**`FALSE`**. The array elements returned are:

| Element | Description                                                                                                                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name    | The name element contains the name of the group. This is a short, usually less than 16 character "handle" of the group, not the real, full name. This should be the same as the `name` parameter used when calling the function, and hence redundant. |
| passwd  | The passwd element contains the group's password in an encrypted format. Often, for example on a system employing "shadow" passwords, an asterisk is returned instead.                                                                                |
| gid     | Group ID of the group in numeric form.                                                                                                                                                                                                                |
| members | This consists of an <span class="type">array</span> of <span class="type">string</span>'s for all the members in the group.                                                                                                                           |

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getgrnam</span>**

``` php
<?php

$groupinfo = posix_getgrnam("toons");

print_r($groupinfo);
?>
```

以上例程的输出类似于：

    Array
    (
        [name]    => toons
        [passwd]  => x
        [members] => Array
            (
                [0] => tom
                [1] => jerry
            )
        [gid]     => 42
    )

### 参见

-   <span class="function">posix\_getegid</span>
-   <span class="function">posix\_getgrgid</span>
-   <span class="function">filegroup</span>
-   <span class="function">stat</span>
-   POSIX man page GETGRNAM(3)

posix\_getgroups
================

Return the group set of the current process

### 说明

<span class="type">array</span> <span
class="methodname">posix\_getgroups</span> ( <span
class="methodparam">void</span> )

Gets the group set of the current process.

### 返回值

Returns an array of integers containing the numeric group ids of the
group set of the current process.

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getgroups</span>**

``` php
<?php

$groups = posix_getgroups();

print_r($groups);
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => 4
        [1] => 20
        [2] => 24
        [3] => 25
        [4] => 29
        [5] => 30
        [6] => 33
        [7] => 44
        [8] => 46
        [9] => 104
        [10] => 109
        [11] => 110
        [12] => 1000
    )

### 参见

-   <span class="function">posix\_getgrgid</span>

posix\_getlogin
===============

Return login name

### 说明

<span class="type">string</span> <span
class="methodname">posix\_getlogin</span> ( <span
class="methodparam">void</span> )

Returns the login name of the user owning the current process.

### 返回值

Returns the login name of the user, as a <span
class="type">string</span>.

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getlogin</span>**

``` php
<?php
echo posix_getlogin(); //apache
?>
```

### 参见

-   <span class="function">posix\_getpwnam</span>
-   POSIX man page GETLOGIN(3)

posix\_getpgid
==============

Get process group id for job control

### 说明

<span class="type"><span class="type">int</span><span
class="type">false</span></span> <span
class="methodname">posix\_getpgid</span> ( <span
class="methodparam"><span class="type">int</span> `$pid`</span> )

Returns the process group identifier of the process `pid`
或者在失败时返回 **`FALSE`**.

### 参数

`pid`  
The process id.

### 返回值

Returns the identifier, as an <span class="type">int</span>.

### 范例

**示例 \#1 Example use of <span class="function">posix\_getpgid</span>**

``` php
<?php
$pid = posix_getppid();
echo posix_getpgid($pid); //35
?>
```

### 注释

> **Note**:
>
> This is a not POSIX function, but is common on BSD and System V
> systems. If the system does not support this function, then it will
> not be included at compile time. This may be checked with <span
> class="function">function\_exists</span>.

### 参见

-   <span class="function">posix\_getppid</span>
-   man page SETPGID(2)

posix\_getpgrp
==============

Return the current process group identifier

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getpgrp</span> ( <span
class="methodparam">void</span> )

Return the process group identifier of the current process.

### 返回值

Returns the identifier, as an <span class="type">int</span>.

### 参见

-   POSIX.1 and the getpgrp(2) manual page on the POSIX system for more
    information on process groups.

posix\_getpid
=============

返回当前进程 id

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getpid</span> ( <span
class="methodparam">void</span> )

Return the process identifier of the current process. 返回当前进程的 id

### 返回值

返回进程 id 号，是整型（<span class="type">integer</span>）。

### 范例

**示例 \#1 <span class="function">posix\_getpid</span> 的使用例子**

``` php
<?php
echo posix_getpid(); //8805
?>
```

### 参见

-   <span class="function">posix\_kill</span>
-   POSIX man page GETPID(2)

posix\_getppid
==============

Return the parent process identifier

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getppid</span> ( <span
class="methodparam">void</span> )

Return the process identifier of the parent process of the current
process.

### 返回值

Returns the identifier, as an <span class="type">int</span>.

### 范例

**示例 \#1 Example use of <span class="function">posix\_getppid</span>**

``` php
<?php
echo posix_getppid(); //8259
?>
```

posix\_getpwnam
===============

Return info about a user by username

### 说明

<span class="type">array</span> <span
class="methodname">posix\_getpwnam</span> ( <span
class="methodparam"><span class="type">string</span> `$username`</span>
)

Returns an <span class="type">array</span> of information about the
given user.

### 参数

`username`  
An alphanumeric username.

### 返回值

On success an array with the following elements is returned, else
**`FALSE`** is returned:

| Element | Description                                                                                                                                                                                                                                                                                                                                                                         |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name    | The name element contains the username of the user. This is a short, usually less than 16 character "handle" of the user, not the real, full name. This should be the same as the `username` parameter used when calling the function, and hence redundant.                                                                                                                         |
| passwd  | The passwd element contains the user's password in an encrypted format. Often, for example on a system employing "shadow" passwords, an asterisk is returned instead.                                                                                                                                                                                                               |
| uid     | User ID of the user in numeric form.                                                                                                                                                                                                                                                                                                                                                |
| gid     | The group ID of the user. Use the function <span class="function">posix\_getgrgid</span> to resolve the group name and a list of its members.                                                                                                                                                                                                                                       |
| gecos   | GECOS is an obsolete term that refers to the finger information field on a Honeywell batch processing system. The field, however, lives on, and its contents have been formalized by POSIX. The field contains a comma separated list containing the user's full name, office phone, office number, and home phone number. On most systems, only the user's full name is available. |
| dir     | This element contains the absolute path to the home directory of the user.                                                                                                                                                                                                                                                                                                          |
| shell   | The shell element contains the absolute path to the executable of the user's default shell.                                                                                                                                                                                                                                                                                         |

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getpwnam</span>**

``` php
<?php

$userinfo = posix_getpwnam("tom");

print_r($userinfo);
?>
```

以上例程的输出类似于：

    Array
    (
        [name]    => tom
        [passwd]  => x
        [uid]     => 10000
        [gid]     => 42
        [gecos]   => "tom,,,"
        [dir]     => "/home/tom"
        [shell]   => "/bin/bash"
    )

### 参见

-   <span class="function">posix\_getpwuid</span>
-   POSIX man page GETPWNAM(3)

posix\_getpwuid
===============

Return info about a user by user id

### 说明

<span class="type">array</span> <span
class="methodname">posix\_getpwuid</span> ( <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

Returns an <span class="type">array</span> of information about the user
referenced by the given user ID.

### 参数

`uid`  
The user identifier.

### 返回值

Returns an associative array with the following elements:

| Element | Description                                                                                                                                                                                                                                                                                                                                                                         |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name    | The name element contains the username of the user. This is a short, usually less than 16 character "handle" of the user, not the real, full name.                                                                                                                                                                                                                                  |
| passwd  | The passwd element contains the user's password in an encrypted format. Often, for example on a system employing "shadow" passwords, an asterisk is returned instead.                                                                                                                                                                                                               |
| uid     | User ID, should be the same as the `uid` parameter used when calling the function, and hence redundant.                                                                                                                                                                                                                                                                             |
| gid     | The group ID of the user. Use the function <span class="function">posix\_getgrgid</span> to resolve the group name and a list of its members.                                                                                                                                                                                                                                       |
| gecos   | GECOS is an obsolete term that refers to the finger information field on a Honeywell batch processing system. The field, however, lives on, and its contents have been formalized by POSIX. The field contains a comma separated list containing the user's full name, office phone, office number, and home phone number. On most systems, only the user's full name is available. |
| dir     | This element contains the absolute path to the home directory of the user.                                                                                                                                                                                                                                                                                                          |
| shell   | The shell element contains the absolute path to the executable of the user's default shell.                                                                                                                                                                                                                                                                                         |

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getpwuid</span>**

``` php
<?php

$userinfo = posix_getpwuid(10000);

print_r($userinfo);
?>
```

以上例程的输出类似于：

    Array
    (
        [name]    => tom
        [passwd]  => x
        [uid]     => 10000
        [gid]     => 42
        [gecos]   => "tom,,,"
        [dir]     => "/home/tom"
        [shell]   => "/bin/bash"
    )

### 参见

-   <span class="function">posix\_getpwnam</span>
-   POSIX man page GETPWNAM(3)

posix\_getrlimit
================

Return info about system resource limits

### 说明

<span class="type">array</span> <span
class="methodname">posix\_getrlimit</span> ( <span
class="methodparam">void</span> )

<span class="function">posix\_getrlimit</span> returns an <span
class="type">array</span> of information about the current resource's
soft and hard limits.

Each resource has an associated soft and hard limit. The soft limit is
the value that the kernel enforces for the corresponding resource. The
hard limit acts as a ceiling for the soft limit. An unprivileged process
may only set its soft limit to a value from 0 to the hard limit, and
irreversibly lower its hard limit.

### 返回值

Returns an associative <span class="type">array</span> of elements for
each limit that is defined. Each limit has a soft and a hard limit.

| Limit name | Limit description                                                                                                                                      |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| core       | The maximum size of the core file. When 0, not core files are created. When core files are larger than this size, they will be truncated at this size. |
| totalmem   | The maximum size of the memory of the process, in bytes.                                                                                               |
| virtualmem | The maximum size of the virtual memory for the process, in bytes.                                                                                      |
| data       | The maximum size of the data segment for the process, in bytes.                                                                                        |
| stack      | The maximum size of the process stack, in bytes.                                                                                                       |
| rss        | The maximum number of virtual pages resident in RAM                                                                                                    |
| maxproc    | The maximum number of processes that can be created for the real user ID of the calling process.                                                       |
| memlock    | The maximum number of bytes of memory that may be locked into RAM.                                                                                     |
| cpu        | The amount of time the process is allowed to use the CPU.                                                                                              |
| filesize   | The maximum size of the data segment for the process, in bytes.                                                                                        |
| openfiles  | One more than the maximum number of open file descriptors.                                                                                             |

### 范例

**示例 \#1 Example use of <span
class="function">posix\_getrlimit</span>**

``` php
<?php

$limits = posix_getrlimit();

print_r($limits);
?>
```

以上例程的输出类似于：

    Array
    (
        [soft core] => 0
        [hard core] => unlimited
        [soft data] => unlimited
        [hard data] => unlimited
        [soft stack] => 8388608
        [hard stack] => unlimited
        [soft totalmem] => unlimited
        [hard totalmem] => unlimited
        [soft rss] => unlimited
        [hard rss] => unlimited
        [soft maxproc] => unlimited
        [hard maxproc] => unlimited
        [soft memlock] => unlimited
        [hard memlock] => unlimited
        [soft cpu] => unlimited
        [hard cpu] => unlimited
        [soft filesize] => unlimited
        [hard filesize] => unlimited
        [soft openfiles] => 1024
        [hard openfiles] => 1024
    )

### 参见

-   man page GETRLIMIT(2)
-   <span class="function">posix\_setrlimit</span>

posix\_getsid
=============

Get the current sid of the process

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getsid</span> ( <span
class="methodparam"><span class="type">int</span> `$pid`</span> )

Return the session id of the process `pid`. The session id of a process
is the process group id of the session leader.

### 参数

`pid`  
The process identifier. If set to 0, the current process is assumed. If
an invalid `pid` is specified, then **`FALSE`** is returned and an error
is set which can be checked with <span
class="function">posix\_get\_last\_error</span>.

### 返回值

Returns the identifier, as an <span class="type">int</span>.

### 范例

**示例 \#1 Example use of <span class="function">posix\_getsid</span>**

``` php
<?php
$pid = posix_getpid();
echo posix_getsid($pid); //8805
?>
```

### 参见

-   <span class="function">posix\_getpgid</span>
-   <span class="function">posix\_setsid</span>
-   POSIX man page GETSID(2)

posix\_getuid
=============

Return the real user ID of the current process

### 说明

<span class="type">int</span> <span
class="methodname">posix\_getuid</span> ( <span
class="methodparam">void</span> )

Return the numeric real user ID of the current process.

### 返回值

Returns the user id, as an <span class="type">int</span>

### 范例

**示例 \#1 Example use of <span class="function">posix\_getuid</span>**

``` php
<?php
echo posix_getuid(); //10000
?>
```

### 参见

-   <span class="function">posix\_getpwuid</span>
-   POSIX man page GETUID(2)

posix\_initgroups
=================

Calculate the group access list

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_initgroups</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">int</span>
`$base_group_id`</span> )

Calculates the group access list for the user specified in name.

### 参数

`name`  
The user to calculate the list for.

`base_group_id`  
Typically the group number from the password file.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   The Unix manual page for initgroups(3).

posix\_isatty
=============

Determine if a file descriptor is an interactive terminal

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_isatty</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> )

Determines if the file descriptor `fd` refers to a valid terminal type
device.

### 参数

`fd`  
The file descriptor, which is expected to be either a file <span
class="type">resource</span> or an <span class="type">integer</span>. An
<span class="type">integer</span> will be assumed to be a file
descriptor that can be passed directly to the underlying system call.

In almost all cases, you will want to provide a file <span
class="type">resource</span>.

### 返回值

Returns **`TRUE`** if `fd` is an open descriptor connected to a terminal
and **`FALSE`** otherwise.

### 参见

-   <span class="function">posix\_ttyname</span>
-   <span class="function">stream\_isatty</span>

posix\_kill
===========

Send a signal to a process

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_kill</span> ( <span class="methodparam"><span
class="type">int</span> `$pid`</span> , <span class="methodparam"><span
class="type">int</span> `$sig`</span> )

Send the signal `sig` to the process with the process identifier `pid`.

### 参数

`pid`  
The process identifier.

`sig`  
One of the
<a href="/pcntl/constants.html" class="link">PCNTL signals constants</a>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   The kill(2) manual page of the POSIX system, which contains
    additional information about negative process identifiers, the
    special pid 0, the special pid -1, and the signal number 0.

posix\_mkfifo
=============

Create a fifo special file (a named pipe)

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_mkfifo</span> ( <span
class="methodparam"><span class="type">string</span> `$pathname`</span>
, <span class="methodparam"><span class="type">int</span> `$mode`</span>
)

<span class="function">posix\_mkfifo</span> creates a special *FIFO*
file which exists in the file system and acts as a bidirectional
communication endpoint for processes.

### 参数

`pathname`  
Path to the *FIFO* file.

`mode`  
The second parameter `mode` has to be given in octal notation (e.g.
0644). The permission of the newly created *FIFO* also depends on the
setting of the current <span class="function">umask</span>. The
permissions of the created file are (mode & \~umask).

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

posix\_mknod
============

Create a special or ordinary file (POSIX.1)

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_mknod</span> ( <span class="methodparam"><span
class="type">string</span> `$pathname`</span> , <span
class="methodparam"><span class="type">int</span> `$mode`</span> \[,
<span class="methodparam"><span class="type">int</span> `$major`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$minor`<span
class="initializer"> = 0</span></span> \]\] )

Creates a special or ordinary file.

### 参数

`pathname`  
The file to create

`mode`  
This parameter is constructed by a bitwise OR between file type (one of
the following constants: **`POSIX_S_IFREG`**, **`POSIX_S_IFCHR`**,
**`POSIX_S_IFBLK`**, **`POSIX_S_IFIFO`** or **`POSIX_S_IFSOCK`**) and
permissions.

`major`  
The major device kernel identifier (required to pass when using
**`S_IFCHR`** or **`S_IFBLK`**).

`minor`  
The minor device kernel identifier.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 A <span class="function">posix\_mknod</span> example**

``` php
<?php

$file = '/tmp/tmpfile';  // file name
$type = POSIX_S_IFBLK;   // file type
$permissions = 0777;     // octal
$major = 1;
$minor = 8;              // /dev/random

if (!posix_mknod($file, $type | $permissions, $major, $minor)) {
    die('Error ' . posix_get_last_error() . ': ' . posix_strerror(posix_get_last_error()));
}

?>
```

### 参见

-   <span class="function">posix\_mkfifo</span>

posix\_setegid
==============

Set the effective GID of the current process

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_setegid</span> ( <span
class="methodparam"><span class="type">int</span> `$gid`</span> )

Set the effective group ID of the current process. This is a privileged
function and needs appropriate privileges (usually root) on the system
to be able to perform this function.

### 参数

`gid`  
The group id.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">posix\_setegid</span> example**

This example will print out the effective group id, once changed.

``` php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setegid(40);
echo 'My real group id is '.posix_getgid(); //20
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### 参见

-   <span class="function">posix\_getgrgid</span>
-   <span class="function">posix\_getgid</span>
-   <span class="function">posix\_setgid</span>

posix\_seteuid
==============

Set the effective UID of the current process

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_seteuid</span> ( <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

Set the effective user ID of the current process. This is a privileged
function and needs appropriate privileges (usually root) on the system
to be able to perform this function.

### 参数

`uid`  
The user id.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">posix\_geteuid</span>
-   <span class="function">posix\_setuid</span>
-   <span class="function">posix\_getuid</span>

posix\_setgid
=============

Set the GID of the current process

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_setgid</span> ( <span
class="methodparam"><span class="type">int</span> `$gid`</span> )

Set the real group ID of the current process. This is a privileged
function and needs appropriate privileges (usually root) on the system
to be able to perform this function. The appropriate order of function
calls is <span class="function">posix\_setgid</span> first, <span
class="function">posix\_setuid</span> last.

> **Note**:
>
> If the caller is a super user, this will also set the effective group
> id.

### 参数

`gid`  
The group id.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">posix\_setgid</span> example**

This example will print out the effective group id, once it is changed.

``` php
<?php
echo 'My real group id is '.posix_getgid(); //20
posix_setgid(40);
echo 'My real group id is '.posix_getgid(); //40
echo 'My effective group id is '.posix_getegid(); //40
?>
```

### 参见

-   <span class="function">posix\_getgrgid</span>
-   <span class="function">posix\_getgid</span>

posix\_setpgid
==============

Set process group id for job control

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_setpgid</span> ( <span
class="methodparam"><span class="type">int</span> `$pid`</span> , <span
class="methodparam"><span class="type">int</span> `$pgid`</span> )

Let the process `pid` join the process group `pgid`.

### 参数

`pid`  
The process id.

`pgid`  
The process group id.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   See POSIX.1 and the setsid(2) manual page on the POSIX system for
    more information on process groups and job control.

posix\_setrlimit
================

Set system resource limits

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_setrlimit</span> ( <span
class="methodparam"><span class="type">int</span> `$resource`</span> ,
<span class="methodparam"><span class="type">int</span>
`$softlimit`</span> , <span class="methodparam"><span
class="type">int</span> `$hardlimit`</span> )

<span class="function">posix\_setrlimit</span> sets the soft and hard
limits for a given system resource.

Each resource has an associated soft and hard limit. The soft limit is
the value that the kernel enforces for the corresponding resource. The
hard limit acts as a ceiling for the soft limit. An unprivileged process
may only set its soft limit to a value from 0 to the hard limit, and
irreversibly lower its hard limit.

### 参数

`resource`  
The
<a href="/posix/constants.html#posix_setrlimit%20constants" class="link">resource limit constant</a>
corresponding to the limit that is being set.

`softlimit`  
The soft limit, in whatever unit the resource limit requires, or
**`POSIX_RLIMIT_INFINITY`**.

`hardlimit`  
The hard limit, in whatever unit the resource limit requires, or
**`POSIX_RLIMIT_INFINITY`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   man page SETRLIMIT(2)
-   <span class="function">posix\_getrlimit</span>

posix\_setsid
=============

Make the current process a session leader

### 说明

<span class="type">int</span> <span
class="methodname">posix\_setsid</span> ( <span
class="methodparam">void</span> )

Make the current process a session leader.

### 返回值

Returns the session id, or -1 on errors.

### 参见

-   The POSIX.1 and the setsid(2) manual page on the POSIX system for
    more information on process groups and job control.

posix\_setuid
=============

Set the UID of the current process

### 说明

<span class="type">bool</span> <span
class="methodname">posix\_setuid</span> ( <span
class="methodparam"><span class="type">int</span> `$uid`</span> )

Set the real user ID of the current process. This is a privileged
function that needs appropriate privileges (usually root) on the system
to be able to perform this function.

### 参数

`uid`  
The user id.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">posix\_setuid</span> example**

This example will show the current user id and then set it to a
different value.

``` php
<?php
echo posix_getuid()."\n"; //10001
echo posix_geteuid()."\n"; //10001
posix_setuid(10000);
echo posix_getuid()."\n"; //10000
echo posix_geteuid()."\n"; //10000
?>
```

### 参见

-   <span class="function">posix\_setgid</span>
-   <span class="function">posix\_seteuid</span>
-   <span class="function">posix\_getuid</span>
-   <span class="function">posix\_geteuid</span>

posix\_strerror
===============

Retrieve the system error message associated with the given errno

### 说明

<span class="type">string</span> <span
class="methodname">posix\_strerror</span> ( <span
class="methodparam"><span class="type">int</span> `$errno`</span> )

Returns the POSIX system error message associated with the given
`errno`. You may get the `errno` parameter by calling <span
class="function">posix\_get\_last\_error</span>.

### 参数

`errno`  
A POSIX error number, returned by <span
class="function">posix\_get\_last\_error</span>. If set to 0, then the
string "Success" is returned.

### 返回值

Returns the error message, as a string.

### 范例

**示例 \#1 <span class="function">posix\_strerror</span> example**

This example will attempt to kill a process which does not exist, then
will print out the corresponding error message.

``` php
<?php
posix_kill(50,SIGKILL);
echo posix_strerror(posix_get_last_error())."\n";
?>
```

以上例程的输出类似于：

    No such process

### 参见

-   <span class="function">posix\_get\_last\_error</span>

posix\_times
============

Get process times

### 说明

<span class="type">array</span> <span
class="methodname">posix\_times</span> ( <span
class="methodparam">void</span> )

Gets information about the current CPU usage.

### 返回值

Returns a hash of strings with information about the current process CPU
usage. The indices of the hash are:

-   <span class="simpara"> ticks - the number of clock ticks that have
    elapsed since reboot. </span>
-   <span class="simpara"> utime - user time used by the current
    process. </span>
-   <span class="simpara"> stime - system time used by the current
    process. </span>
-   <span class="simpara"> cutime - user time used by current process
    and children. </span>
-   <span class="simpara"> cstime - system time used by current process
    and children. </span>

### 注释

**Warning**

This function isn't reliable to use, it may return negative values for
high times.

### 范例

**示例 \#1 Example use of <span class="function">posix\_times</span>**

``` php
<?php

$times = posix_times();

print_r($times);
?>
```

以上例程的输出类似于：

    Array
    (
        [ticks] => 25814410
        [utime] => 1
        [stime] => 1
        [cutime] => 0
        [cstime] => 0
    )

posix\_ttyname
==============

Determine terminal device name

### 说明

<span class="type">string</span> <span
class="methodname">posix\_ttyname</span> ( <span
class="methodparam"><span class="type">mixed</span> `$fd`</span> )

Returns a <span class="type">string</span> for the absolute path to the
current terminal device that is open on the file descriptor `fd`.

### 参数

`fd`  
The file descriptor, which is expected to be either a file <span
class="type">resource</span> or an <span class="type">integer</span>. An
<span class="type">integer</span> will be assumed to be a file
descriptor that can be passed directly to the underlying system call.

In almost all cases, you will want to provide a file <span
class="type">resource</span>.

### 返回值

On success, returns a <span class="type">string</span> of the absolute
path of the `fd`. On failure, returns **`FALSE`**

posix\_uname
============

Get system name

### 说明

<span class="type">array</span> <span
class="methodname">posix\_uname</span> ( <span
class="methodparam">void</span> )

Gets information about the system.

Posix requires that assumptions must not be made about the format of the
values, e.g. the assumption that a release may contain three digits or
anything else returned by this function.

### 返回值

Returns a hash of strings with information about the system. The indices
of the hash are

-   <span class="simpara"> sysname - operating system name (e.g. Linux)
    </span>
-   <span class="simpara"> nodename - system name (e.g. valiant) </span>
-   <span class="simpara"> release - operating system release (e.g.
    2.2.10) </span>
-   <span class="simpara"> version - operating system version (e.g. \#4
    Tue Jul 20 17:01:36 MEST 1999) </span>
-   <span class="simpara"> machine - system architecture (e.g. i586)
    </span>
-   <span class="simpara"> domainname - DNS domainname (e.g.
    example.com) </span>

domainname is a GNU extension and not part of POSIX.1, so this field is
only available on GNU systems or when using the GNU libc.

### 范例

**示例 \#1 Example use of <span class="function">posix\_uname</span>**

``` php
<?php
$uname=posix_uname();
print_r($uname);
?>
```

以上例程的输出类似于：

    Array
    (
        [sysname] => Linux
        [nodename] => funbox
        [release] => 2.6.20-15-server
        [version] => #2 SMP Sun Apr 15 07:41:34 UTC 2007
        [machine] => i686
    )

**目录**

-   [posix\_access](/ref/posix.html#posix_access) — Determine
    accessibility of a file
-   [posix\_ctermid](/ref/posix.html#posix_ctermid) — Get path name of
    controlling terminal
-   [posix\_errno](/ref/posix.html#posix_errno) — 别名
    posix\_get\_last\_error
-   [posix\_get\_last\_error](/ref/posix.html#posix_get_last_error) —
    Retrieve the error number set by the last posix function that failed
-   [posix\_getcwd](/ref/posix.html#posix_getcwd) — Pathname of current
    directory
-   [posix\_getegid](/ref/posix.html#posix_getegid) — Return the
    effective group ID of the current process
-   [posix\_geteuid](/ref/posix.html#posix_geteuid) — Return the
    effective user ID of the current process
-   [posix\_getgid](/ref/posix.html#posix_getgid) — Return the real
    group ID of the current process
-   [posix\_getgrgid](/ref/posix.html#posix_getgrgid) — Return info
    about a group by group id
-   [posix\_getgrnam](/ref/posix.html#posix_getgrnam) — Return info
    about a group by name
-   [posix\_getgroups](/ref/posix.html#posix_getgroups) — Return the
    group set of the current process
-   [posix\_getlogin](/ref/posix.html#posix_getlogin) — Return login
    name
-   [posix\_getpgid](/ref/posix.html#posix_getpgid) — Get process group
    id for job control
-   [posix\_getpgrp](/ref/posix.html#posix_getpgrp) — Return the current
    process group identifier
-   [posix\_getpid](/ref/posix.html#posix_getpid) — 返回当前进程 id
-   [posix\_getppid](/ref/posix.html#posix_getppid) — Return the parent
    process identifier
-   [posix\_getpwnam](/ref/posix.html#posix_getpwnam) — Return info
    about a user by username
-   [posix\_getpwuid](/ref/posix.html#posix_getpwuid) — Return info
    about a user by user id
-   [posix\_getrlimit](/ref/posix.html#posix_getrlimit) — Return info
    about system resource limits
-   [posix\_getsid](/ref/posix.html#posix_getsid) — Get the current sid
    of the process
-   [posix\_getuid](/ref/posix.html#posix_getuid) — Return the real user
    ID of the current process
-   [posix\_initgroups](/ref/posix.html#posix_initgroups) — Calculate
    the group access list
-   [posix\_isatty](/ref/posix.html#posix_isatty) — Determine if a file
    descriptor is an interactive terminal
-   [posix\_kill](/ref/posix.html#posix_kill) — Send a signal to a
    process
-   [posix\_mkfifo](/ref/posix.html#posix_mkfifo) — Create a fifo
    special file (a named pipe)
-   [posix\_mknod](/ref/posix.html#posix_mknod) — Create a special or
    ordinary file (POSIX.1)
-   [posix\_setegid](/ref/posix.html#posix_setegid) — Set the effective
    GID of the current process
-   [posix\_seteuid](/ref/posix.html#posix_seteuid) — Set the effective
    UID of the current process
-   [posix\_setgid](/ref/posix.html#posix_setgid) — Set the GID of the
    current process
-   [posix\_setpgid](/ref/posix.html#posix_setpgid) — Set process group
    id for job control
-   [posix\_setrlimit](/ref/posix.html#posix_setrlimit) — Set system
    resource limits
-   [posix\_setsid](/ref/posix.html#posix_setsid) — Make the current
    process a session leader
-   [posix\_setuid](/ref/posix.html#posix_setuid) — Set the UID of the
    current process
-   [posix\_strerror](/ref/posix.html#posix_strerror) — Retrieve the
    system error message associated with the given errno
-   [posix\_times](/ref/posix.html#posix_times) — Get process times
-   [posix\_ttyname](/ref/posix.html#posix_ttyname) — Determine terminal
    device name
-   [posix\_uname](/ref/posix.html#posix_uname) — Get system name
