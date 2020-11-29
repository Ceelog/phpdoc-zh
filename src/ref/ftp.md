ftp\_alloc
==========

为要上传的文件分配空间

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_alloc</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">int</span> `$filesize`</span> \[,
<span class="methodparam"><span class="type">string</span>
`&$result`</span> \] )

向远程 FTP 服务器发送 *ALLO* 命令， 来为要上传的文件分配空间。

> **Note**:
>
> 很多 FTP 服务器不支持*ALLO* 命令。
> 如果服务器不支持此命令，将会返回错误码（**`FALSE`**），
> 返回成功码（**`TRUE`**）表示预分配空间不是必需的，
> 客户端可以继续操作了。
> 因此，请仅对需要强制预分配空间服务器使用此函数。

### 参数

`ftp_stream`  
FTP 连接标示符。

`filesize`  
要分配的空间，以字节为单位。

`result`  
如果提供此参数，那么服务器的响应 会以文本方式设置到 `result` 中。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_alloc</span> 函数例程**

``` php
<?php

$file = "/home/user/myfile";

// 连接服务器
$conn_id = ftp_connect('ftp.example.com');
$login_result = ftp_login($conn_id, 'anonymous', 'user@example.com');

if (ftp_alloc($conn_id, filesize($file), $result)) {
  echo "Space successfully allocated on server.  Sending $file.\n";
  ftp_put($conn_id, '/incomming/myfile', $file, FTP_BINARY);
} else {
  echo "Unable to allocate space on server.  Server said: $result\n";
}

ftp_close($conn_id);

?>
```

### 参见

-   <span class="function">ftp\_put</span>
-   <span class="function">ftp\_fput</span>

ftp\_append
===========

Append the contents of a file to another file on the FTP server

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_append</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp`</span> , <span
class="methodparam"><span class="type">string</span>
`$remote_file`</span> , <span class="methodparam"><span
class="type">string</span> `$local_file`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = **`FTP_BINARY`**</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ftp`  

`remote_file`  

`local_file`  

`mode`  

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

ftp\_cdup
=========

切换到当前目录的父目录

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_cdup</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> )

切换目录至当前目录的父目录 (上级目录)。

### 参数

`ftp_stream`  
FTP 连接的标识符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_cdup</span> 例子**

``` php
<?php 
// set up basic connection 
$conn_id = ftp_connect($ftp_server); 

// login with username and password 
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass); 

// change the current directory to html 
ftp_chdir($conn_id, 'html'); 

echo ftp_pwd($conn_id); // /html 

// return to the parent directory 
if (ftp_cdup($conn_id)) { 
  echo "cdup successful\n"; 
} else { 
  echo "cdup not successful\n"; 
} 

echo ftp_pwd($conn_id); // / 

ftp_close($conn_id); 
?>
```

### 参见

-   <span class="function">ftp\_chdir</span>
-   <span class="function">ftp\_pwd</span>

ftp\_chdir
==========

在 FTP 服务器上改变当前目录

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_chdir</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

将当前目录切换为指定的目录。

### 参数

`ftp_stream`  
FTP 连接的标识符。

`directory`  
目标目录。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回
**`FALSE`**。如果切换目录失败，PHP 还会发出一条警告。

### 范例

**示例 \#1 <span class="function">ftp\_chdir</span> 例子**

``` php
<?php

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// check connection
if ((!$conn_id) || (!$login_result)) {
    die("FTP connection has failed !");
}

echo "Current directory: " . ftp_pwd($conn_id) . "\n";

// try to change the directory to somedir
if (ftp_chdir($conn_id, "somedir")) {
    echo "Current directory is now: " . ftp_pwd($conn_id) . "\n";
} else {
    echo "Couldn't change directory\n";
}

// close the connection 
ftp_close($conn_id); 
?>
```

### 参见

-   <span class="function">ftp\_cdup</span>
-   <span class="function">ftp\_pwd</span>

ftp\_chmod
==========

设置 FTP 服务器上的文件权限

### 说明

<span class="type">int</span> <span class="methodname">ftp\_chmod</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> , <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

将服务器上的文件权限设置为 `mode` 指定的值。

### 参数

`ftp_stream`  
FTP 连接标示符。

`mode`  
要设置的权限值， *八进制* 值。

`filename`  
远程文件名称。

### 返回值

操作成功返回文件新的权限，操作失败返回 **`FALSE`** 。

### 范例

**示例 \#1 <span class="function">ftp\_chmod</span> 函数例程**

``` php
<?php
$file = 'public_html/index.php';

// 建立基础连接
$conn_id = ftp_connect($ftp_server);

// 使用用户名和密码登录
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// 尝试设置 $file 的权限为 644
if (ftp_chmod($conn_id, 0644, $file) !== false) {
 echo "$file chmoded successfully to 644\n";
} else {
 echo "could not chmod $file\n";
}

// 关闭连接
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">chmod</span>

ftp\_close
==========

关闭一个 FTP 连接

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> )

<span class="function">ftp\_close</span>
关闭给出的连接标识符并释放资源。

> **Note**:
>
> 调用本函数后，将不能再使用 FTP 连接，必须用 <span
> class="function">ftp\_connect</span> 建立一个新连接。

### 参数

`ftp_stream`  
FTP 连接的标识符。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_close</span> 例子**

``` php
<?php

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// print the current directory
echo ftp_pwd($conn_id); // /

// close this connection
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_connect</span>

ftp\_connect
============

建立一个新的 FTP 连接

### 说明

<span class="type">resource</span> <span
class="methodname">ftp\_connect</span> ( <span class="methodparam"><span
class="type">string</span> `$host`</span> \[, <span
class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 21</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 90</span></span> \]\] )

<span class="function">ftp\_connect</span> 将会建立一个 FTP
连接到指定的服务器 `host`。

### 参数

`host`  
要连接的服务器地址。此参数后面不应以斜线结尾，前面也不需要用 *ftp://*
开头。

`port`  
为要连接到的 FTP 器的端口号，如果没有设置或者为 0，则会使用默认的端口 21
来连接。

`timeout`  
用来设置网络传输的超时时间限制。如果此选项留空，则默认的值为 90
秒。超时时间可以在任何时候通过函数 <span
class="function">ftp\_set\_option</span> 及 <span
class="function">ftp\_get\_option</span> 来改变和获取。

### 返回值

如果成功返回一个 FTP 连接资源句柄，发生错误则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_connect</span> 示例**

``` php
<?php

$ftp_server = "ftp.example.com";

// set up a connection or die
$conn_id = ftp_connect($ftp_server) or die("Couldn't connect to $ftp_server"); 

?>
```

### 参见

-   <span class="function">ftp\_close</span>
-   <span class="function">ftp\_ssl\_connect</span>

ftp\_delete
===========

删除 FTP 服务器上的一个文件

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_delete</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$path`</span> )

<span class="function">ftp\_delete</span> 函数用来删除 FTP
服务器上的一个由参数 `path` 指定的的文件。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`path`  
要删除的文件。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_delete</span> 例子**

``` php
<?php
$file = 'public_html/old.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to delete $file
if (ftp_delete($conn_id, $file)) {
 echo "$file deleted successful\n";
} else {
 echo "could not delete $file\n";
}

// close the connection
ftp_close($conn_id);
?>
```

ftp\_exec
=========

在 FTP 服务器运行指定的命令

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_exec</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$command`</span> )

发送一个 SITE EXEC `command` 请求到 FTP 服务器。

### 参数

`ftp_stream`  
FTP 连接资源句柄。

`command`  
要执行的命令。

### 返回值

如果执行成功（服务器发送响应代码 *200*）则返回 **`TRUE`**；否则返回
**`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_exec</span> 示例**

``` php
<?php

// variable initialization
$command = 'ls -al >files.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// execute command
if (ftp_exec($conn_id, $command)) {
    echo "$command executed successfully\n";
} else {
    echo "could not execute $command\n";
}

// close the connection
ftp_close($conn_id);

?>
```

### 参见

-   <span class="function">ftp\_raw</span>

ftp\_fget
=========

从 FTP 服务器上下载一个文件并保存到本地一个已经打开的文件中

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_fget</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">resource</span> `$handle`</span> , <span
class="methodparam"><span class="type">string</span>
`$remote_file`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">int</span> `$resumepos`<span
class="initializer"> = 0</span></span> \] )

<span class="function">ftp\_fget</span> 函数用来下载由 `remote_file`
指定的文件，并写入到本地已经被打开的一个文件中。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`handle`  
本地已经打开的文件的句柄。

`remote_file`  
远程文件的路径。

`mode`  
传送模式参数， 必须是 (文本模式) **`FTP_ASCII`** 或 (二进制模式)
**`FTP_BINARY`** 中的一个。

`resumepos`  
远程文件开始下载的位置。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_fget</span> 例子**

``` php
<?php

// path to remote file
$remote_file = 'somefile.txt';
$local_file = 'localfile.txt';

// open some file to write to
$handle = fopen($local_file, 'w');

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to download $remote_file and save it to $handle
if (ftp_fget($conn_id, $handle, $remote_file, FTP_ASCII, 0)) {
 echo "successfully written to $local_file\n";
} else {
 echo "There was a problem while downloading $remote_file to $local_file\n";
}

// close the connection and the file handler
ftp_close($conn_id);
fclose($handle);
?>
```

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 4.3.0 | 增加了`resumepos` 的支持。 |

### 参见

-   <span class="function">ftp\_get</span>
-   <span class="function">ftp\_nb\_get</span>
-   <span class="function">ftp\_nb\_fget</span>

ftp\_fput
=========

上传一个已经打开的文件到 FTP 服务器

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_fput</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
, <span class="methodparam"><span class="type">int</span> `$mode`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$startpos`<span class="initializer"> = 0</span></span> \] )

<span class="function">ftp\_fput</span>
函数用来上传一个在已经打开的文件中的数据到 FTP 服务器。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`remote_file`  
远程文件路径。

`handle`  
打开的本地文件句柄，读取到文件末尾。

`mode`  
传输模式只能为 (文本模式) **`FTP_ASCII`** 或 (二进制模式)
**`FTP_BINARY`** 其中的一个。

`startpos`  
远程文件上传的开始位置。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_fput</span> 例子**

``` php
<?php

// open some file for reading
$file = 'somefile.txt';
$fp = fopen($file, 'r');

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to upload $file
if (ftp_fput($conn_id, $file, $fp, FTP_ASCII)) {
    echo "Successfully uploaded $file\n";
} else {
    echo "There was a problem while uploading $file\n";
}

// close the connection and the file handler
ftp_close($conn_id);
fclose($fp);

?>
```

### 更新日志

| 版本  | 说明                       |
|-------|----------------------------|
| 4.3.0 | 添加了 `startpos` 的支持。 |

### 参见

-   <span class="function">ftp\_put</span>
-   <span class="function">ftp\_nb\_fput</span>
-   <span class="function">ftp\_nb\_put</span>

ftp\_get\_option
================

返回当前 FTP 连接的各种不同的选项设置

### 说明

<span class="type">mixed</span> <span
class="methodname">ftp\_get\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> )

此函数会返回连接句柄为 `ftp_stream`，指定键值 `option` 的值。

### 参数

`ftp_stream`  
FTP 连接资源句柄。

`option`  
截止到目前，支持的选项有：

|                       |                                                     |
|-----------------------|-----------------------------------------------------|
| **`FTP_TIMEOUT_SEC`** | 返回当前设定的网络操作的超时时间。                  |
| **`FTP_AUTOSEEK`**    | 此选项打开时返回 **`TRUE`**，否则返回 **`FALSE`**。 |

### 返回值

如果成功则返回选项的值，否则，如果给定的参数 `option` 选项不被支持则返回
**`FALSE`**，同时会抛出一条警告（warning）信息。

### 范例

**示例 \#1 <span class="function">ftp\_get\_option</span> 示例**

``` php
<?php
// Get the timeout of the given FTP stream
$timeout = ftp_get_option($conn_id, FTP_TIMEOUT_SEC);
?>
```

### 参见

-   <span class="function">ftp\_set\_option</span>

ftp\_get
========

从 FTP 服务器上下载一个文件

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_get</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$local_file`</span> , <span
class="methodparam"><span class="type">string</span>
`$remote_file`</span> , <span class="methodparam"><span
class="type">int</span> `$mode`</span> \[, <span
class="methodparam"><span class="type">int</span> `$resumepos`<span
class="initializer"> = 0</span></span> \] )

<span class="function">ftp\_get</span> 函数用来下载 FTP
服务器上指定的文件并保存为本地文件。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`local_file`  
文件本地的路径（如果文件已经存在，则会被覆盖）。

`remote_file`  
文件的远程路径。

`mode`  
传送模式。只能为 (文本模式) **`FTP_ASCII`** 或 (二进制模式)
**`FTP_BINARY`** 中的其中一个。

`resumepos`  
从远程文件的这个位置继续下载。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_get</span> 例子**

``` php
<?php

// define some variables
$local_file = 'local.zip';
$server_file = 'server.zip';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to download $server_file and save to $local_file
if (ftp_get($conn_id, $local_file, $server_file, FTP_BINARY)) {
    echo "Successfully written to $local_file\n";
} else {
    echo "There was a problem\n";
}

// close the connection
ftp_close($conn_id);

?>
```

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 4.3.0 | 增加了 `resumepos`。 |

### 参见

-   <span class="function">ftp\_pasv</span>
-   <span class="function">ftp\_fget</span>
-   <span class="function">ftp\_nb\_get</span>
-   <span class="function">ftp\_nb\_fget</span>

ftp\_login
==========

登录 FTP 服务器

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_login</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$username`</span>
, <span class="methodparam"><span class="type">string</span>
`$password`</span> )

使用用户名和密码登录入给定的 FTP 连接。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`username`  
用户名（*USER*）。

`password`  
密码（*PASS*）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。 如果登录失败，PHP
会抛出一个警告。

### 范例

**示例 \#1 <span class="function">ftp\_login</span> 例子**

``` php
<?php
                     
$ftp_server = "ftp.example.com";
$ftp_user = "foo";
$ftp_pass = "bar";

// 设置一个连接或失败时退出
$conn_id = ftp_connect($ftp_server) or die("Couldn't connect to $ftp_server"); 

// 尝试登录
if (@ftp_login($conn_id, $ftp_user, $ftp_pass)) {
    echo "Connected as $ftp_user@$ftp_server\n";
} else {
    echo "Couldn't connect as $ftp_user\n";
}

// 关闭连接
ftp_close($conn_id);  
?>
```

ftp\_mdtm
=========

返回指定文件的最后修改时间

### 说明

<span class="type">int</span> <span class="methodname">ftp\_mdtm</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> )

<span class="function">ftp\_mdtm</span> 获取远程文件的最后修改时间。

> **Note**:
>
> 某些 FTP 服务器可能会不支持这个特性！

> **Note**:
>
> <span class="function">ftp\_mdtm</span> 不适用于检查目录。

### 参数

`ftp_stream`  
FTP 连接句柄。

`remote_file`  
要检查的远程文件。

### 返回值

返回指定文件的最后修改时间，以 UNIX
时间戳的方式返回。如果发生错误，或文件不存在则返回 -1。

### 范例

**示例 \#1 <span class="function">ftp\_mdtm</span> 示例**

``` php
<?php

$file = 'somefile.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

//  get the last modified time
$buff = ftp_mdtm($conn_id, $file);

if ($buff != -1) {
    // somefile.txt was last modified on: March 26 2003 14:16:41.
    echo "$file was last modified on : " . date("F d Y H:i:s.", $buff);
} else {
    echo "Couldn't get mdtime";
}

// close the connection
ftp_close($conn_id);

?>
```

ftp\_mkdir
==========

建立新目录

### 说明

<span class="type">string</span> <span
class="methodname">ftp\_mkdir</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

在 FTP 服务器上，创建指定的目录 `directory`。

### 参数

`ftp_stream`  
FTP 连接句柄。

`directory`  
要创建的目录名。

### 返回值

如果成功返回新建的目录名，发生错误时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_mkdir</span> example**

``` php
<?php

$dir = 'www';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to create the directory $dir
if (ftp_mkdir($conn_id, $dir)) {
 echo "successfully created $dir\n";
} else {
 echo "There was a problem while creating $dir\n";
}

// close the connection
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_rmdir</span>

ftp\_mlsd
=========

Returns a list of files in the given directory

### 说明

<span class="type">array</span> <span
class="methodname">ftp\_mlsd</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

### 参数

`ftp_stream`  
The link identifier of the FTP connection.

`directory`  
The directory to be listed.

### 返回值

Returns an array of arrays with file infos from the specified directory
on success or **`FALSE`** on error.

### 范例

**示例 \#1 <span class="function">ftp\_mlsd</span> example**

``` php
<?php

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// get contents of the current directory
$contents = ftp_mlsd($conn_id, ".");

// output $contents
var_dump($contents);

?>
```

以上例程的输出类似于：

    array(5) {
      [0]=>
      array(8) {
        ["name"]=>
        string(1) "."
        ["modify"]=>
        string(14) "20171212154511"
        ["perm"]=>
        string(7) "flcdmpe"
        ["type"]=>
        string(4) "cdir"
        ["unique"]=>
        string(11) "811U5740002"
        ["UNIX.group"]=>
        string(2) "33"
        ["UNIX.mode"]=>
        string(4) "0755"
        ["UNIX.owner"]=>
        string(2) "33"
      }
      [1]=>
      array(8) {
        ["name"]=>
        string(2) ".."
        ["modify"]=>
        string(14) "20171212154511"
        ["perm"]=>
        string(7) "flcdmpe"
        ["type"]=>
        string(4) "pdir"
        ["unique"]=>
        string(11) "811U5740002"
        ["UNIX.group"]=>
        string(2) "33"
        ["UNIX.mode"]=>
        string(4) "0755"
        ["UNIX.owner"]=>
        string(2) "33"
      }
      [2]=>
      array(8) {
        ["name"]=>
        string(11) "public_html"
        ["modify"]=>
        string(14) "20171211171525"
        ["perm"]=>
        string(7) "flcdmpe"
        ["type"]=>
        string(3) "dir"
        ["unique"]=>
        string(11) "811U5740525"
        ["UNIX.group"]=>
        string(2) "33"
        ["UNIX.mode"]=>
        string(4) "0755"
        ["UNIX.owner"]=>
        string(2) "33"
      }
      [3]=>
      array(8) {
        ["name"]=>
        string(10) "public_ftp"
        ["modify"]=>
        string(14) "20171211174536"
        ["perm"]=>
        string(7) "flcdmpe"
        ["type"]=>
        string(3) "dir"
        ["unique"]=>
        string(11) "811U57405EE"
        ["UNIX.group"]=>
        string(2) "33"
        ["UNIX.mode"]=>
        string(4) "0755"
        ["UNIX.owner"]=>
        string(2) "33"
      }
      [4]=>
      array(8) {
        ["name"]=>
        string(3) "www"
        ["modify"]=>
        string(14) "www"
        ["perm"]=>
        string(7) "flcdmpe"
        ["type"]=>
        string(3) "dir"
        ["unique"]=>
        string(11) "811U5740780"
        ["UNIX.group"]=>
        string(2) "33"
        ["UNIX.mode"]=>
        string(4) "0755"
        ["UNIX.owner"]=>
        string(2) "33"
      }
    }

### 参见

-   <span class="function">ftp\_rawlist</span>
-   <span class="function">ftp\_nlist</span>

ftp\_nb\_continue
=================

连续获取／发送文件（以不分块的方式 non-blocking）

### 说明

<span class="type">int</span> <span
class="methodname">ftp\_nb\_continue</span> ( <span
class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> )

以不分块的方式，连续获取/发送文件。

### 参数

`ftp_stream`  
FTP 连接句柄。

### 返回值

返回 **`FTP_FAILED`** 或 **`FTP_FINISHED`** 或 **`FTP_MOREDATA`**.

### 范例

**示例 \#1 <span class="function">ftp\_nb\_continue</span> 示例**

``` php
<?php

// Initiate the download
$ret = ftp_nb_get($my_connection, "test", "README", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Continue downloading...
   $ret = ftp_nb_continue($my_connection);
}
if ($ret != FTP_FINISHED) {
   echo "There was an error downloading the file...";
   exit(1);
}
?>
```

ftp\_nb\_fget
=============

从 FTP 服务器获取文件并写入到一个打开的文件（非阻塞）

### 说明

<span class="type">int</span> <span
class="methodname">ftp\_nb\_fget</span> ( <span
class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">resource</span> `$handle`</span> , <span
class="methodparam"><span class="type">string</span>
`$remote_file`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
**`FTP_IMAGE`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$resumepos`<span class="initializer"> =
0</span></span> \]\] )

<span class="function">ftp\_nb\_fget</span> 从远程 FTP
服务器获取一个文件

本函数和 <span class="function">ftp\_fget</span> 函数的区别是
本函数是异步方式获取文件的，
所以在下载文件的过程中你的程序还可以执行其他操作。

### 参数

`ftp_stream`  
FTP 连接标示符。

`handle`  
用来存储数据的一个已经打开的文件句柄。

`remote_file`  
远程文件路径。

`mode`  
传输模式，必须是 **`FTP_ASCII`** 或者 **`FTP_BINARY`**。

`resumepos`  
远程文件开始下载的位置（即从远程文件的哪个字节开始下载）。

### 返回值

返回 **`FTP_FAILED`** 或 **`FTP_FINISHED`** 或 **`FTP_MOREDATA`**。

### 更新日志

| 版本  | 说明                                                          |
|-------|---------------------------------------------------------------|
| 7.3.0 | 参数 `mode` 变为可选参数。 在之前的版本中，这是一个必填参数。 |

### 范例

**示例 \#1 <span class="function">ftp\_nb\_fget</span> 函数例程**

``` php
<?php

// 打开要写入的文件
$file = 'index.php';
$fp = fopen($file, 'w');

$conn_id = ftp_connect($ftp_server);

$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// 初始化下载
$ret = ftp_nb_fget($conn_id, $fp, $file, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // 其他要做的工作
   echo ".";

   // 继续下载...
   $ret = ftp_nb_continue($conn_id);
}
if ($ret != FTP_FINISHED) {
   echo "There was an error downloading the file...";
   exit(1);
}

// 关闭文件句柄
fclose($fp);
?>
```

### 参见

-   <span class="function">ftp\_nb\_get</span>
-   <span class="function">ftp\_nb\_continue</span>
-   <span class="function">ftp\_fget</span>
-   <span class="function">ftp\_get</span>

ftp\_nb\_fput
=============

将文件存储到 FTP 服务器 （非阻塞）

### 说明

<span class="type">int</span> <span
class="methodname">ftp\_nb\_fput</span> ( <span
class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> , <span
class="methodparam"><span class="type">resource</span> `$handle`</span>
\[, <span class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = **`FTP_IMAGE`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$startpos`<span
class="initializer"> = 0</span></span> \]\] )

<span class="function">ftp\_nb\_fput</span> 把已打开的文件内容存储到远程
FTP 服务器

本函数和 <span class="function">ftp\_fput</span> 函数的区别是
本函数是异步上传文件。
所以在文件上传过程中，你的程序还可以执行其他操作。

### 参数

`ftp_stream`  
FTP 连接标示符。

`remote_file`  
远程文件路径。

`handle`  
已经打开的本地文件指针，当读取到文件末尾时结束。

`mode`  
传输模式。必须是 **`FTP_ASCII`** 或 **`FTP_BINARY`**。

`startpos`  
要将文件存储到远程文件的开始位置（即从远程文件的哪个字节位置开始存储）。

### 返回值

返回 **`FTP_FAILED`** 或 **`FTP_FINISHED`** 或 **`FTP_MOREDATA`**。

### 更新日志

| 版本  | 说明                                                          |
|-------|---------------------------------------------------------------|
| 7.3.0 | 参数 `mode` 变为可选参数。 在之前的版本中，这是一个必填参数。 |

### 范例

**示例 \#1 <span class="function">ftp\_nb\_fput</span> 函数例程**

``` php
<?php

$file = 'index.php';

$fp = fopen($file, 'r');

$conn_id = ftp_connect($ftp_server);

$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// 初始化上传
$ret = ftp_nb_fput($conn_id, $file, $fp, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // 任何其他需要做的操作
   echo ".";

   // 继续上传...
   $ret = ftp_nb_continue($conn_id);
}
if ($ret != FTP_FINISHED) {
   echo "There was an error uploading the file...";
   exit(1);
}

fclose($fp);
?>
```

### 参见

-   <span class="function">ftp\_nb\_put</span>
-   <span class="function">ftp\_nb\_continue</span>
-   <span class="function">ftp\_put</span>
-   <span class="function">ftp\_fput</span>

ftp\_nb\_get
============

从 FTP 服务器上获取文件并写入本地文件（non-blocking）

### 说明

<span class="type">int</span> <span
class="methodname">ftp\_nb\_get</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span>
`$local_file`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = **`FTP_BINARY`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$resumepos`<span
class="initializer"> = 0</span></span> \]\] )

<span class="function">ftp\_nb\_get</span> 在 FTP
服务器上获取指定的远程文件，并保存到本地。

和 <span class="function">ftp\_get</span>
不同之处，在于此函数是通过异步的方式来获取文件，这意味着，你的程序可以在下载文件的同时，同步进行其它操作。

### 参数

`ftp_stream`  
FTP 连接句柄。

`local_file`  
保存到的本地文件路径（如果文件已存在会被覆盖）。

`remote_file`  
远程文件路径。

`mode`  
指定传输模式。必须是 **`FTP_ASCII`** 或 **`FTP_BINARY`**。

`resumepos`  
开始下载文件的起始位置。

### 返回值

返回 **`FTP_FAILED`** 或 **`FTP_FINISHED`** 或 **`FTP_MOREDATA`**。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.3.0 | `mode` 参数变为可选，之前是强制性的。 |

### 范例

**示例 \#1 <span class="function">ftp\_nb\_get</span> 示例**

``` php
<?php

// 初始化
$ret = ftp_nb_get($my_connection, "test", "README", FTP_BINARY);
while ($ret == FTP_MOREDATA) {
   
   // 可以同步干其它事
   echo ".";

   // 继续下载...
   $ret = ftp_nb_continue($my_connection);
}
if ($ret != FTP_FINISHED) {
   echo "下载文件出错...";
   exit(1);
}
?>
```

**示例 \#2 通过 <span class="function">ftp\_nb\_get</span>
恢复下载一个文件**

``` php
<?php

// 初始化 
$ret = ftp_nb_get($my_connection, "test", "README", FTP_BINARY, 
                      filesize("test"));
// OR: $ret = ftp_nb_get($my_connection, "test", "README", 
//                           FTP_BINARY, FTP_AUTORESUME);
while ($ret == FTP_MOREDATA) {
   
   // 做你爱做的事
   echo ".";

   // 继续下载Ing...
   $ret = ftp_nb_continue($my_connection);
}
if ($ret != FTP_FINISHED) {
   echo "下载文件出错...";
   exit(1);
}
?>
```

**示例 \#3 使用 <span class="function">ftp\_nb\_get</span>
从指定位置恢复下载文件**

``` php
<?php

// 禁止 Autoseek
ftp_set_option($my_connection, FTP_AUTOSEEK, false);

// 初始化
$ret = ftp_nb_get($my_connection, "newfile", "README", FTP_BINARY, 100);
while ($ret == FTP_MOREDATA) {

   /* ... */
   
   // 继续下载...
   $ret = ftp_nb_continue($my_connection);
}
?>
```

在上面的示例中，`newfile` 会比 FTP 服务器上的 `README` 文件小 100
bytes，因为开始下载的时候设置了偏移量为 100。如果我们不禁止
**`FTP_AUTOSEEK`**，则 `newfile` 文件前面的 100 bytes 会变成 *'\\0'*。

### 参见

-   <span class="function">ftp\_nb\_fget</span>
-   <span class="function">ftp\_nb\_continue</span>
-   <span class="function">ftp\_fget</span>
-   <span class="function">ftp\_get</span>

ftp\_nb\_put
============

存储一个文件至 FTP 服务器（non-blocking）

### 说明

<span class="type">int</span> <span
class="methodname">ftp\_nb\_put</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span>
`$remote_file`</span> , <span class="methodparam"><span
class="type">string</span> `$local_file`</span> \[, <span
class="methodparam"><span class="type">int</span> `$mode`<span
class="initializer"> = **`FTP_BINARY`**</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$startpos`<span
class="initializer"> = 0</span></span> \]\] )

<span class="function">ftp\_nb\_put</span> 函数用来把本地文件
`local_file` 存储到 FTP 服务器上由 `remote_file` 参数指定的路径。

与函数 <span class="function">ftp\_put</span>
不同的是，此函数上传文件的时候采用的是异步传输模式，也就意味着在文件传送的过程中，你的程序可以继续干其它的事情。

### 参数

`ftp_stream`  
FTP 连接的链接标识符。

`remote_file`  
远程文件路径。

`local_file`  
本地文件路径。

`mode`  
传输模式选择，可选参数为 **`FTP_ASCII`**（文本模式）或
**`FTP_BINARY`**（二进制模式）。

`startpos`  
指定传输开始的位置，用来续传支持。

### 返回值

返回 **`FTP_FAILED`** 或 **`FTP_FINISHED`** 或 **`FTP_MOREDATA`**。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.3.0 | `mode` 参数为可选，之前版本中为必填。 |

### 范例

**示例 \#1 <span class="function">ftp\_nb\_put</span> 示例**

``` php
<?php

// 初始化
$ret = ftp_nb_put($my_connection, "test.remote", "test.local", FTP_BINARY);
while ($ret == FTP_MOREDATA) {
   
   // 可以同时干其它事
   echo ".";

   // 继续上传...
   $ret = ftp_nb_continue($my_connection);
}
if ($ret != FTP_FINISHED) {
   echo "上传过程中发生错误...";
   exit(1);
}
?>
```

**示例 \#2 使用 <span class="function">ftp\_nb\_put</span> 来续传文件**

``` php
<?php

// 初始化
$ret = ftp_nb_put($my_connection, "test.remote", "test.local", 
                      FTP_BINARY, ftp_size("test.remote"));
// 另一种写法: $ret = ftp_nb_put($my_connection, "test.remote", "test.local", 
//                           FTP_BINARY, FTP_AUTORESUME);

while ($ret == FTP_MOREDATA) {
   
   // 可以同时干其它事情
   echo ".";

   // 继续上传...
   $ret = ftp_nb_continue($my_connection);
}
if ($ret != FTP_FINISHED) {
   echo "上传过程中发生错误...";
   exit(1);
}
?>
```

### 参见

-   <span class="function">ftp\_nb\_fput</span>
-   <span class="function">ftp\_nb\_continue</span>
-   <span class="function">ftp\_put</span>
-   <span class="function">ftp\_fput</span>

ftp\_nlist
==========

返回给定目录的文件列表

### 说明

<span class="type">array</span> <span
class="methodname">ftp\_nlist</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

### 参数

`ftp_stream`  
FTP 连接资源。

`directory`  
指定要列表的目录。本参数接受带参数的形式，例如： ftp\_nlist($conn\_id,
"-la /you/dir");
注意此参数不对传入值做处理，在目录或者文件名包括空格或特殊的情况下，可能会存在问题。

### 返回值

如果成功则返回给定目录下的文件名组成的数组，否则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_nlist</span> 例子**

``` php
<?php

// set up basic connection
$conn_id = ftp_connect($ftp_server);
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// check connection
if ((!$conn_id) || (!$login_result)) {
    die("FTP connection has failed !");
}
 
// get contents of the root directory
$contents = ftp_nlist($conn_id, "/");

// output $contents
var_dump($contents);

?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      string(11) "public_html"
      [1]=>
      string(10) "public_ftp"
      [2]=>
      string(3) "www"

### 参见

-   <span class="function">ftp\_rawlist</span>
-   <span class="function">ftp\_mlsd</span>

ftp\_pasv
=========

返回当前 FTP 被动模式是否打开

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_pasv</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">bool</span> `$pasv`</span> )

在被动模式打开的情况下，数据的传送由客户机启动，而不是由服务器开始。

请注意 <span class="function">ftp\_pasv</span> 只能在 FTP
登录成功后方可调用，否则会失败。

### 参数

`ftp_stream`  
FTP 连接资源。

`pasv`  
如果参数 `pasv` 为 **`TRUE`**，打开被动模式传输 (PASV MODE)
，否则则关闭被动传输模式。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_pasv</span> 实例**

``` php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// turn passive mode on
ftp_pasv($conn_id, true);

// upload a file
if (ftp_put($conn_id, $remote_file, $file, FTP_ASCII)) {
 echo "successfully uploaded $file\n";
} else {
 echo "There was a problem while uploading $file\n";
}

// close the connection
ftp_close($conn_id);
?>
```

ftp\_put
========

上传文件到 FTP 服务器

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_put</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> , <span
class="methodparam"><span class="type">string</span>
`$local_file`</span> \[, <span class="methodparam"><span
class="type">int</span> `$mode`<span class="initializer"> =
**`FTP_BINARY`**</span></span> \[, <span class="methodparam"><span
class="type">int</span> `$startpos`<span class="initializer"> =
0</span></span> \]\] )

<span class="function">ftp\_put</span> 函数用来上传指定的本地文件到 FTP
服务器。

### 参数

`ftp_stream`  
FTP 连接资源。

`remote_file`  
远程文件路径。

`local_file`  
本地文件路径。

`mode`  
传送模式，只能为 **`FTP_ASCII`**（文本模式）或
**`FTP_BINARY`**（二进制模式）。

`startpos`  
指定开始上传的位置，一般用来文件续传。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 7.3.0 | `mode` 参数为可选，之前版本中为必选。 |

### 范例

**示例 \#1 <span class="function">ftp\_put</span> 实例**

``` php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// upload a file
if (ftp_put($conn_id, $remote_file, $file, FTP_ASCII)) {
 echo "successfully uploaded $file\n";
} else {
 echo "There was a problem while uploading $file\n";
}

// close the connection
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_pasv</span>
-   <span class="function">ftp\_fput</span>
-   <span class="function">ftp\_nb\_fput</span>
-   <span class="function">ftp\_nb\_put</span>

ftp\_pwd
========

返回当前目录名

### 说明

<span class="type">string</span> <span
class="methodname">ftp\_pwd</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> )

### 参数

`ftp_stream`  
FTP 连接资源。

### 返回值

返回当前目录名称，发生错误则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_pwd</span> 例子**

``` php
<?php

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// change directory to public_html
ftp_chdir($conn_id, 'public_html');

// print current directory
echo ftp_pwd($conn_id); // /public_html

// close the connection
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_chdir</span>
-   <span class="function">ftp\_cdup</span>

ftp\_quit
=========

<span class="function">ftp\_close</span> 的 别名

### 说明

此函数是该函数的别名： <span class="function">ftp\_close</span>

ftp\_raw
========

向 FTP 服务器发送命令

### 说明

<span class="type">array</span> <span class="methodname">ftp\_raw</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$command`</span> )

向 FTP 服务器发送任意 `command`。

### 参数

`ftp_stream`  
FTP 连接标示符。

`command`  
要执行的命令。

### 返回值

将服务器的响应以字符串数组的形式返回。 对于响应内容既不做解析处理，
也不检测命令是否执行成功。

### 范例

**示例 \#1 使用 <span class="function">ftp\_raw</span> 登录远程 FTP
服务器**

``` php
<?php
$fp = ftp_connect("ftp.example.com");

/* 等同于
   ftp_login($fp, "joeblow", "secret"); */
ftp_raw($fp, "USER joeblow");
ftp_raw($fp, "PASS secret");
?>
```

### 参见

-   <span class="function">ftp\_exec</span>

ftp\_rawlist
============

返回指定目录下文件的详细列表

### 说明

<span class="type">array</span> <span
class="methodname">ftp\_rawlist</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = **`FALSE`**</span></span> \] )

<span class="function">ftp\_rawlist</span> 函数将执行 FTP **LIST**
命令，并把结果做为一个数组返回。

### 参数

`ftp_stream`  
FTP 连接资源。

`directory`  
要操作的目录路径，可以包括 **LIST** 参数。

`recursive`  
如果此参数为 **`TRUE`**，实际执行的命令将会为 **LIST -R**。

### 返回值

返回一个数组，数组的每个元素为返回文本的每一行，输出结构不会被解析。使用函数
<span class="function">ftp\_systype</span> 可以用来判断 FTP
服务器的类型，从而可以用来判断返回列表的类型。

The output is not parsed in any way. The system type identifier returned
by <span class="function">ftp\_systype</span> can be used to determine
how the results should be interpreted.

### 范例

**示例 \#1 <span class="function">ftp\_rawlist</span> 示例**

``` php
<?php

// 初始化连接
$conn_id = ftp_connect($ftp_server);

// 使用用户名和密码登录
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// 获取 / 路径下的文件列表
$buff = ftp_rawlist($conn_id, '/');

// 关闭连接
ftp_close($conn_id);

// 输出
var_dump($buff);
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      string(65) "drwxr-x---   3 vincent  vincent      4096 Jul 12 12:16 public_ftp"
      [1]=>
      string(66) "drwxr-x---  15 vincent  vincent      4096 Nov  3 21:31 public_html"
      [2]=>
      string(73) "lrwxrwxrwx   1 vincent  vincent        11 Jul 12 12:16 www -> public_html"
    }

### 参见

-   <span class="function">ftp\_nlist</span>
-   <span class="function">ftp\_mlsd</span>

ftp\_rename
===========

更改 FTP 服务器上的文件或目录名

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_rename</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$oldname`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newname`</span> )

<span class="function">ftp\_rename</span> 将 FTP
服务器上的一个文件或目录改名。

### 参数

`ftp_stream`  
FTP 连接的标识符。

`oldname`  
原来的文件／目录名。

`newname`  
新名字。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
失败时（比如试图重命名一个不存在的文件）将会抛出一个 *E\_WARNING*
错误信息。

### 范例

**示例 \#1 <span class="function">ftp\_rename</span> 例子**

``` php
<?php
$old_file = 'somefile.txt.bak';
$new_file = 'somefile.txt';

// set up basic connection
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// try to rename $old_file to $new_file
if (ftp_rename($conn_id, $old_file, $new_file)) {
    echo "successfully renamed $old_file to $new_file\n";
} else {
    echo "There was a problem while renaming $old_file to $new_file\n";
}

// close the connection
ftp_close($conn_id);
?>
```

ftp\_rmdir
==========

删除 FTP 服务器上的一个目录

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_rmdir</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> , <span
class="methodparam"><span class="type">string</span> `$directory`</span>
)

删除由参数 `directory` 指定的目录。

### 参数

`ftp_stream`  
FTP 连接资源。

`directory`  
要删除的目录，必须是一个空目录的绝对路径或相对路径。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_rmdir</span> 例子**

``` php
<?php
$dir = 'www/';

$conn_id = ftp_connect($ftp_server);
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

if (ftp_rmdir($conn_id, $dir)) {
    echo 'Successfully deleted ' . $dir;
} else {
    echo 'There was a problem while deleting ' . $dir;
}

ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_mkdir</span>

ftp\_set\_option
================

设置各种 FTP 运行时选项

### 说明

<span class="type">bool</span> <span
class="methodname">ftp\_set\_option</span> ( <span
class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">int</span> `$option`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

本函数控制指定 FTP 流的各种运行时选项。

### 参数

`ftp_stream`  
FTP 连接的标识符。

`option`  
目前支持以下选项：

|                          |                                                                                                                                         |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **`FTP_TIMEOUT_SEC`**    | 改变网络传输的超时时间。参数 `value` 必须为整数且大于 0。默认的超时时间为 90 秒。                                                       |
| **`FTP_AUTOSEEK`**       | 当此选项打开时，带 `resumepos` 或 `startpos` 参数的GET 或 PUT 请求 将先检索到文件中指定的位置。此选项默认是打开的。                     |
| **`FTP_USEPASVADDRESS`** | 当此选项禁用时，PHP 会忽略掉 FTP 服务器通过 PASV 命令返回的 IP 地址，直接使用在 ftp\_connect() 中指定的地址。`value` 参数必须是布尔型。 |

`value`  
本参数取决于要修改哪个 `option`。

### 返回值

如果选项能够被设置，返回 **`TRUE`**，否则返回 **`FALSE`**。如果参数
`option` 不被支持或者给定的参数 `value` 的值与参数 `option`
不匹配，则会同时返回一条警告信息。

### 范例

**示例 \#1 <span class="function">ftp\_set\_option</span> 例子**

``` php
<?php
// 设置网络传输超时时间为 10 秒
ftp_set_option($conn_id, FTP_TIMEOUT_SEC, 10);
?>
```

### 参见

-   <span class="function">ftp\_get\_option</span>

ftp\_site
=========

向服务器发送 SITE 命令

### 说明

<span class="type">bool</span> <span class="methodname">ftp\_site</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$command`</span> )

<span class="function">ftp\_site</span> 函数向 FTP
服务器发送指定的命令。

*SITE*
命令是非标准化的，不同的服务器不尽相同。主要用于处理文件权限以及组成员等事情。

### 参数

`ftp_stream`  
FTP 连接资源。

`command`  
SITE
命令。注意本参数没有经过处理，在文件名有存在空格或其它特殊字符的情况下可能会有问题。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 向一个 FTP 服务器发送一条 SITE 命令**

``` php
<?php
// 连接 FTP 服务器
$conn = ftp_connect('ftp.example.com');
if (!$conn) die('无法连接到 ftp.example.com');

// 使用用户 user 和密码 pass 登录服务器
if (!ftp_login($conn, 'user', 'pass')) die('登录失败到 ftp.example.com');

// Issue: "SITE CHMOD 0600 /home/user/privatefile" command to ftp server
if (ftp_site($conn, 'CHMOD 0600 /home/user/privatefile')) {
   echo "命令执行成功。\n";
} else {
   die('命令执行失败。');
}
?>
```

### 参见

-   <span class="function">ftp\_raw</span>

ftp\_size
=========

返回指定文件的大小

### 说明

<span class="type">int</span> <span class="methodname">ftp\_size</span>
( <span class="methodparam"><span class="type">resource</span>
`$ftp_stream`</span> , <span class="methodparam"><span
class="type">string</span> `$remote_file`</span> )

<span class="function">ftp\_size</span> 函数以字节返回远程文件
`remote_file` 的大小。如果指定文件不存在或发生错误，则返回 -1。有些 FTP
服务器可能不支持此特性。

> **Note**:
>
> 获取成功返回文件大小，否则返回 -1。

### 参数

`ftp_stream`  
FTP 连接资源。

`remote_file`  
远程文件。

### 返回值

执行成功返回文件大小，失败返回 -1。

### 范例

**示例 \#1 <span class="function">ftp\_size</span> 例子**

``` php
<?php
$file = 'somefile.txt';

// set up basic connection 
$conn_id = ftp_connect($ftp_server);

// login with username and password
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// get the size of $file
$res = ftp_size($conn_id, $file);

if ($res != -1) {
    echo "size of $file is $res bytes";
} else {
    echo "couldn't get the size";
}

//close the conntion
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_rawlist</span>

ftp\_ssl\_connect
=================

打开 SSL-FTP 连接

### 说明

<span class="type">resource</span> <span
class="methodname">ftp\_ssl\_connect</span> ( <span
class="methodparam"><span class="type">string</span> `$host`</span> \[,
<span class="methodparam"><span class="type">int</span> `$port`<span
class="initializer"> = 21</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$timeout`<span
class="initializer"> = 90</span></span> \]\] )

<span class="function">ftp\_ssl\_connect</span> *显式*的打开一个到
`host` 的安全 FTP 连接（SSL-FTP）。 即使服务器未配置
SSL-FTP，或者服务器的证书无效，<span
class="function">ftp\_ssl\_connect</span>
函数也会成功的建立到服务器的连接。直到调用 <span
class="function">ftp\_login</span> 函数的时候， 客户端才会发送对应的
AUTH FTP 命令，此时，如果服务器未配置 SSL-FTP 或者整数无效， <span
class="function">ftp\_login</span> 函数会失败。

> **Note**: **为何本函数有可能不存在？**  
>
> 只有 PHP 构建时同时包含了 ftp 模块 和
> <a href="/ref/openssl.html" class="link">OpenSSL</a> 模块时， <span
> class="function">ftp\_ssl\_connect</span> 函数才可用。 也就是说，在
> Windows 平台上，官方发布的 PHP 构建中本函数不可用。 如果需要在 Windows
> 平台使用本函数，需要自行编译 PHP。

> **Note**:
>
> <span class="function">ftp\_ssl\_connect</span> 不是用来连接 sFTP
> 服务的。 要在 PHP 中使用 sFTP，请参见 <span
> class="function">ssh2\_sftp</span>。

### 参数

`host`  
FTP 服务器地址。 此参数末尾不可以有斜线，开头也不可以有 *ftp://*。

`port`  
要连接的端口。如果省略此参数或设置为 0，将使用 FTP 默认端口 21。

`timeout`  
此参数设置所有后续网络操作的超时时长。 如果省略，默认值为 90 秒。
可以使用 <span class="function">ftp\_set\_option</span> 和 <span
class="function">ftp\_get\_option</span> 函数随时读取或设置超时时长。

### 返回值

操作成功返回 SSL-FTP 流，操作失败返回 **`FALSE`** 。

### 更新日志

| 版本  | 说明                                                                                                 |
|-------|------------------------------------------------------------------------------------------------------|
| 5.2.2 | 以前版本中，如果无法使用 SSL 连接，将会返回一个非 SSL 的连接， 在 5.2.2 版本中修改为返回 **`FALSE`** |

### 范例

**示例 \#1 <span class="function">ftp\_ssl\_connect</span> 函数例程**

``` php
<?php

// 建立基础 SSL 连接
$conn_id = ftp_ssl_connect($ftp_server);

// 使用用户名和密码登录
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

if (!$login_result) {
    // 在这种情况下，PHP 会发生 E_WARNING 级别的告警消息
    die("can't login");
}

echo ftp_pwd($conn_id); // /

// 关闭 ssl 连接
ftp_close($conn_id);
?>
```

### 参见

-   <span class="function">ftp\_connect</span>

ftp\_systype
============

返回远程 FTP 服务器的操作系统类型

### 说明

<span class="type">string</span> <span
class="methodname">ftp\_systype</span> ( <span class="methodparam"><span
class="type">resource</span> `$ftp_stream`</span> )

返回远程 FTP 服务器的操作系统类型。

### 参数

`ftp_stream`  
FTP 连接资源。

### 返回值

返回远程服务器类型，发生错误则返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">ftp\_systype</span> 示例**

``` php
<?php
// 建立 ftp 连接
$ftp = ftp_connect('ftp.example.com');
ftp_login($ftp, 'user', 'password');

// 获取操作系统类型
if ($type = ftp_systype($ftp)) {
    echo "Example.com 的操作系统为 $type\n";
} else {
    echo "无法获取操作系统类型";
}
?>
```

以上例程的输出类似于：

    Example.com 的操作系统为 UNIX

**目录**

-   [ftp\_alloc](/ref/ftp.html#ftp_alloc) — 为要上传的文件分配空间
-   [ftp\_append](/ref/ftp.html#ftp_append) — Append the contents of a
    file to another file on the FTP server
-   [ftp\_cdup](/ref/ftp.html#ftp_cdup) — 切换到当前目录的父目录
-   [ftp\_chdir](/ref/ftp.html#ftp_chdir) — 在 FTP 服务器上改变当前目录
-   [ftp\_chmod](/ref/ftp.html#ftp_chmod) — 设置 FTP 服务器上的文件权限
-   [ftp\_close](/ref/ftp.html#ftp_close) — 关闭一个 FTP 连接
-   [ftp\_connect](/ref/ftp.html#ftp_connect) — 建立一个新的 FTP 连接
-   [ftp\_delete](/ref/ftp.html#ftp_delete) — 删除 FTP
    服务器上的一个文件
-   [ftp\_exec](/ref/ftp.html#ftp_exec) — 在 FTP 服务器运行指定的命令
-   [ftp\_fget](/ref/ftp.html#ftp_fget) — 从 FTP
    服务器上下载一个文件并保存到本地一个已经打开的文件中
-   [ftp\_fput](/ref/ftp.html#ftp_fput) — 上传一个已经打开的文件到 FTP
    服务器
-   [ftp\_get\_option](/ref/ftp.html#ftp_get_option) — 返回当前 FTP
    连接的各种不同的选项设置
-   [ftp\_get](/ref/ftp.html#ftp_get) — 从 FTP 服务器上下载一个文件
-   [ftp\_login](/ref/ftp.html#ftp_login) — 登录 FTP 服务器
-   [ftp\_mdtm](/ref/ftp.html#ftp_mdtm) — 返回指定文件的最后修改时间
-   [ftp\_mkdir](/ref/ftp.html#ftp_mkdir) — 建立新目录
-   [ftp\_mlsd](/ref/ftp.html#ftp_mlsd) — Returns a list of files in the
    given directory
-   [ftp\_nb\_continue](/ref/ftp.html#ftp_nb_continue) —
    连续获取／发送文件（以不分块的方式 non-blocking）
-   [ftp\_nb\_fget](/ref/ftp.html#ftp_nb_fget) — 从 FTP
    服务器获取文件并写入到一个打开的文件（非阻塞）
-   [ftp\_nb\_fput](/ref/ftp.html#ftp_nb_fput) — 将文件存储到 FTP 服务器
    （非阻塞）
-   [ftp\_nb\_get](/ref/ftp.html#ftp_nb_get) — 从 FTP
    服务器上获取文件并写入本地文件（non-blocking）
-   [ftp\_nb\_put](/ref/ftp.html#ftp_nb_put) — 存储一个文件至 FTP
    服务器（non-blocking）
-   [ftp\_nlist](/ref/ftp.html#ftp_nlist) — 返回给定目录的文件列表
-   [ftp\_pasv](/ref/ftp.html#ftp_pasv) — 返回当前 FTP 被动模式是否打开
-   [ftp\_put](/ref/ftp.html#ftp_put) — 上传文件到 FTP 服务器
-   [ftp\_pwd](/ref/ftp.html#ftp_pwd) — 返回当前目录名
-   [ftp\_quit](/ref/ftp.html#ftp_quit) — ftp\_close 的 别名
-   [ftp\_raw](/ref/ftp.html#ftp_raw) — 向 FTP 服务器发送命令
-   [ftp\_rawlist](/ref/ftp.html#ftp_rawlist) —
    返回指定目录下文件的详细列表
-   [ftp\_rename](/ref/ftp.html#ftp_rename) — 更改 FTP
    服务器上的文件或目录名
-   [ftp\_rmdir](/ref/ftp.html#ftp_rmdir) — 删除 FTP 服务器上的一个目录
-   [ftp\_set\_option](/ref/ftp.html#ftp_set_option) — 设置各种 FTP
    运行时选项
-   [ftp\_site](/ref/ftp.html#ftp_site) — 向服务器发送 SITE 命令
-   [ftp\_size](/ref/ftp.html#ftp_size) — 返回指定文件的大小
-   [ftp\_ssl\_connect](/ref/ftp.html#ftp_ssl_connect) — 打开 SSL-FTP
    连接
-   [ftp\_systype](/ref/ftp.html#ftp_systype) — 返回远程 FTP
    服务器的操作系统类型
