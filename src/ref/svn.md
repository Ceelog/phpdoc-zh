svn\_add
========

计划在工作目录添加项

### 说明

<span class="type">bool</span> <span class="methodname">svn\_add</span>
( <span class="methodparam"><span class="type">string</span>
`$path`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$recursive`<span class="initializer"> =
true</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$force`<span class="initializer"> =
false</span></span> \]\] )

添加文件, 目录或者链接在`路径` 到工作目录。将在下一次执行<span
class="function">svn\_commit</span> 时把工作副本添加到项目中。

### 参数

`path`  
添加项的路径。

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`recursive`  
如果添加项为目录是否递归目录下所有文件。 默认为 **`TRUE`**

`force`  
If true, Subversion will recurse into already versioned directories in
order to add unversioned files that may be hiding in those directories.
Default is **`FALSE`**

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 <span class="function">svn\_add</span> 例子**

在工作目录使用命令 **`svn status`** 返回值:

``` examples
$ svn status
?      foobar.txt
```

...代码:

``` php
<?php
svn_add('foobar.txt');
?>
```

...计划 `foobar.txt` 文件添加到版本库。

### 参见

-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.add.html" class="link external">» SVN documentation on svn add</a>

svn\_auth\_get\_parameter
=========================

Retrieves authentication parameter

### 说明

<span class="type">string</span> <span
class="methodname">svn\_auth\_get\_parameter</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> )

Retrieves authentication parameter at `key`. For a list of valid keys
and their meanings, consult the
<a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">authentication constants list</a>.

### 参数

`key`  
String key name. Use the
<a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">authentication constants</a>
defined by this extension to specify a key.

### 返回值

Returns the string value of the parameter at `key`; returns **`NULL`**
if parameter does not exist.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <span class="function">svn\_auth\_set\_parameter</span>
-   <a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">Authentication constants</a>

svn\_auth\_set\_parameter
=========================

Sets an authentication parameter

### 说明

<span class="type">void</span> <span
class="methodname">svn\_auth\_set\_parameter</span> ( <span
class="methodparam"><span class="type">string</span> `$key`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

Sets authentication parameter at `key` to `value`. For a list of valid
keys and their meanings, consult the
<a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">authentication constants list</a>.

### 参数

`key`  
String key name. Use the
<a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">authentication constants</a>
defined by this extension to specify a key.

`value`  
String value to set to parameter at key. Format of value varies with the
parameter.

### 返回值

没有返回值。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Default authentication example**

This example configures SVN so that the default username to use is 'Bob'
and the default password is 'abc123':

``` php
<?php
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_USERNAME, 'Bob');
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_PASSWORD, 'abc123');
?>
```

### 参见

-   <span class="function">svn\_auth\_get\_parameter</span>
-   <a href="/svn/constants.html#Constants%20usable%20with%20svn_auth_set_parameter" class="link">Authentication constants</a>

svn\_blame
==========

Get the SVN blame for a file

### 说明

<span class="type">array</span> <span
class="methodname">svn\_blame</span> ( <span class="methodparam"><span
class="type">string</span> `$repository_url`</span> \[, <span
class="methodparam"><span class="type">int</span> `$revision_no`<span
class="initializer"> = SVN\_REVISION\_HEAD</span></span> \] )

Get the SVN blame of a file from a repository URL.

### 参数

`repository_url`  
The repository URL.

`revision_no`  
The revision number.

### 返回值

An <span class="type">array</span> of SVN blame information separated by
line which includes the revision number, line number, line of code,
author, and date.

### 范例

**示例 \#1 <span class="function">svn\_blame</span> example**

``` php
<?php
$svnurl = 'http://svn.example.org/svnroot/foo/trunk/index.php';

print_r( svn_blame($svnurl) );

?>
```

以上例程的输出类似于：

    Array
    (
        [0] = Array
              (
               [rev] = 1
               [line_no] = 1
               [line] = Hello World
               [author] = joesmith
               [date] = 2007-07-02T05:51:26.628396Z
              )
        [1] = Array
              ...

### 参见

-   <span class="function">svn\_diff</span>
-   <span class="function">svn\_logs</span>
-   <span class="function">svn\_status</span>

svn\_cat
========

Returns the contents of a file in a repository

### 说明

<span class="type">string</span> <span
class="methodname">svn\_cat</span> ( <span class="methodparam"><span
class="type">string</span> `$repos_url`</span> \[, <span
class="methodparam"><span class="type">int</span> `$revision_no`</span>
\] )

Returns the contents of the URL `repos_url` to a file in the repository,
optionally at revision number `revision_no`.

### 参数

`repos_url`  
String URL path to item in a repository.

`revision_no`  
Integer revision number of item to retrieve, default is the HEAD
revision.

### 返回值

Returns the string contents of the item from the repository on success,
and **`FALSE`** on failure.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example retrieves the contents of a file at revision 28:

``` php
<?php
$contents = svn_cat('http://www.example.com/svnroot/calc/gui.c', 28)
?>
```

### 参见

-   <span class="function">svn\_list</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.cat.html" class="link external">» SVN documentation on svn cat</a>

svn\_checkout
=============

Checks out a working copy from the repository

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_checkout</span> ( <span
class="methodparam"><span class="type">string</span> `$repos`</span> ,
<span class="methodparam"><span class="type">string</span>
`$targetpath`</span> \[, <span class="methodparam"><span
class="type">int</span> `$revision`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \]\] )

Checks out a working copy from the repository at `repos` to `targetpath`
at revision `revision`.

### 参数

`repos`  
String URL path to directory in repository to check out.

`targetpath`  
String local path to directory to check out in to

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`revision`  
Integer revision number of repository to check out. Default is HEAD, the
most recent revision.

`flags`  
Any combination of **`SVN_NON_RECURSIVE`** and
**`SVN_IGNORE_EXTERNALS`**.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates how to check out a directory from a repository
to a directory named calc:

``` php
<?php
svn_checkout('http://www.example.com/svnroot/calc/trunk', dirname(__FILE__) . '/calc');
?>
```

The *dirname(\_\_FILE\_\_)* call is necessary in order to convert the
calc relative path into an absolute one. If calc exists, you can also
use <span class="function">realpath</span> to retrieve an absolute path.

### 参见

-   <span class="function">svn\_add</span>
-   <span class="function">svn\_commit</span>
-   <span class="function">svn\_status</span>
-   <span class="function">svn\_update</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.checkout.html" class="link external">» SVN documentation on svn checkout</a>

svn\_cleanup
============

Recursively cleanup a working copy directory, finishing incomplete
operations and removing locks

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_cleanup</span> ( <span class="methodparam"><span
class="type">string</span> `$workingdir`</span> )

Recursively cleanup working copy directory `workingdir`, finishing any
incomplete operations and removing working copy locks. Use when a
working copy is in limbo and needs to be usable again.

### 参数

`workingdir`  
String path to local working directory to cleanup

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates clean up of a working copy in a directory
named help-me:

``` php
<?php
svn_cleanup(realpath('help-me'));
?>
```

The <span class="function">realpath</span> call is necessary due to
SVN's quirky handling of relative paths.

### 参见

-   <span class="function">update</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.cleanup.html" class="link external">» SVN documentation on svn cleanup</a>

svn\_client\_version
====================

Returns the version of the SVN client libraries

### 说明

<span class="type">string</span> <span
class="methodname">svn\_client\_version</span> ( <span
class="methodparam">void</span> )

Returns the version of the SVN client libraries

### 返回值

String version number, usually in form of x.y.z.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

``` php
<?php
echo svn_client_version();
?>
```

以上例程的输出类似于：

    1.3.1

svn\_commit
===========

将修改的本地文件副本发送至版本库

### 说明

<span class="type">array</span> <span
class="methodname">svn\_commit</span> ( <span class="methodparam"><span
class="type">string</span> `$log`</span> , <span
class="methodparam"><span class="type">array</span> `$targets`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$recursive`<span class="initializer"> = true</span></span> \] )

提交本地文件副本的改变使用参数 `targets` ，使用 `log`
参数作为提交日志，`targets` 参数默认使用递归，`recursive` 参数设置为
**`FALSE`** 将不使用递归。

> **Note**: <span class="simpara">
> 此方法没有指定任何认证参数，用户名和密码必须使用 <span
> class="function">svn\_auth\_set\_parameter</span> </span>

### 参数

`log`  
长文本的提交日志

`targets`  
本地文件路径数组

**Warning**
此参数必须是一个数组，一个单一字符串是不被接收的。

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`recursive`  
布尔类型，是否禁用 `targets` 递归。默认值为 **`TRUE`**

### 返回值

返回数组信息如下:

``` returnvalues
array(
    0 => 提交版本号
    1 => ISO 8601 格式的提交时间
    2 => 提交者
)
```

失败返回 **`FALSE`**

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 基本示例**

这个例子是将一个计算程序目录提交到一个版本库，使用用户名为 Bob
以及密码为 abc123 (提倡可以使用强密码)

``` php
<?php
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_USERNAME, 'Bob');
svn_auth_set_parameter(SVN_AUTH_PARAM_DEFAULT_PASSWORD, 'abc123');
var_dump(svn_commit('Log message of Bob\'s commit', array(realpath('calculator'))));
?>
```

以上例程会输出：

    array(
      0 => 1415,
      1 => '2007-05-26T01:44:28.453125Z',
      2 => 'Bob'
    )

### 参见

-   <span class="function">svn\_auth\_set\_parameter</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.commit.html" class="link external">» 参见 svn 官方文档</a>

svn\_delete
===========

Delete items from a working copy or repository

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_delete</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$force`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Deletes the file, directory or symbolic link at `path` from the working
directory. The item will be deleted from the repository the next time
you call <span class="function">svn\_commit</span> on the working copy.

### 参数

`path`  
Path of item to delete.

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`force`  
If **`TRUE`**, the file will be deleted even if it has local
modifications. Otherwise, local modifications will result in a failure.
Default is **`FALSE`**

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 参见

-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.delete.html" class="link external">» SVN documentation on svn delete</a>

svn\_diff
=========

Recursively diffs two paths

### 说明

<span class="type">array</span> <span
class="methodname">svn\_diff</span> ( <span class="methodparam"><span
class="type">string</span> `$path1`</span> , <span
class="methodparam"><span class="type">int</span> `$rev1`</span> , <span
class="methodparam"><span class="type">string</span> `$path2`</span> ,
<span class="methodparam"><span class="type">int</span> `$rev2`</span> )

Recursively diffs two paths, `path1` and `path2`.

> **Note**:
>
> This is not a general-purpose diff utility. Only local files that are
> versioned may be diffed: other files will fail.

### 参数

`path1`  
First path to diff. This can be a URL to a file/directory in an SVN
repository or a local file/directory path.

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

**Warning**
If a local file path has only backslashes and no forward slashes, this
extension will fail to find the path. Always replace all backslashes
with forward slashes when using this function.

`rev1`  
First path's revision number. Use **`SVN_REVISION_HEAD`** to specify the
most recent revision.

`path2`  
Second path to diff. See `path1` for description.

`rev2`  
Second path's revision number. See `rev1` for description.

### 返回值

Returns an array-list consisting of two streams: the first is the diff
output and the second contains error stream output. The streams can be
read using <span class="function">fread</span>. Returns **`FALSE`** or
**`NULL`** on error.

The diff output will, by default, be in the form of Subversion's custom
unified diff format, but an
<a href="http://svnbook.red-bean.com/en/1.2/svn.advanced.externaldifftools.html" class="link external">» external diff engine</a>
may be used depending on Subversion's configuration.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates the basic usage of this function, and the
retrieval of contents from the stream:

``` php
<?php
list($diff, $errors) = svn_diff(
    'http://www.example.com/svnroot/trunk/foo', SVN_REVISION_HEAD,
    'http://www.example.com/svnroot/branches/dev/foo', SVN_REVISION_HEAD
);
if (!$diff) exit;
$contents = '';
while (!feof($diff)) {
  $contents .= fread($diff, 8192);
}
fclose($diff);
fclose($errors);
var_dump($contents);
?>
```

以上例程会输出：

    Index: http://www.example.com/svnroot/trunk/foo
    ===================================================================
    --- http://www.example.com/svnroot/trunk/foo        (.../foo) (revision 23)
    +++ http://www.example.com/svnroot/branches/dev/foo (.../foo) (revision 27)
     // further diff output

**示例 \#2 Diffing two revisions of a repository path**

This example implements a wrapper function that allows a user to easily
diff two revisions of the same item using an external repository path
(the default syntax is somewhat verbose):

``` php
<?php
function svn_diff_same_item($path, $rev1, $rev2) {
    return svn_diff($path, $rev1, $path, $rev2);
}
?>
```

**示例 \#3 Portably diffing two local files**

This example implements a wrapper function that portably diffs two local
files, compensating for the <span class="function">realpath</span> fix
and the backslashes bug:

``` php
<?php
function svn_diff_local($path1, $rev1, $path2, $rev2) {
    $path1 = str_replace('\\', '/', realpath($path1));
    $path2 = str_replace('\\', '/', realpath($path2));
    return svn_diff($path1, $rev1, $path2, $rev2);
}
?>
```

### 参见

-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.diff.html" class="link external">» SVN documentation on svn diff</a>

svn\_export
===========

Export the contents of a SVN directory

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_export</span> ( <span class="methodparam"><span
class="type">string</span> `$frompath`</span> , <span
class="methodparam"><span class="type">string</span> `$topath`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$working_copy`<span class="initializer"> = **`TRUE`**</span></span> \[,
<span class="methodparam"><span class="type">int</span>
`$revision_no`<span class="initializer"> = -1</span></span> \]\] )

Export the contents of either a working copy or repository into a
'clean' directory.

### 参数

`frompath`  
The path to the current repository.

`topath`  
The path to the new repository.

`working_copy`  
If **`TRUE`**, it will export uncommitted files from the working copy.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">svn\_export</span> example**

``` php
<?php
$working_dir     = '../';
$new_working_dir = '/home/user/devel/foo/trunk';

svn_export($working_dir, $new_working_dir);
?>
```

### 参见

-   <span class="function">svn\_import</span>

svn\_fs\_abort\_txn
===================

Abort a transaction, returns true if everything is okay, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_abort\_txn</span> ( <span
class="methodparam"><span class="type">resource</span> `$txn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Abort a transaction, returns true if everything is okay, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_apply\_text
====================

Creates and returns a stream that will be used to replace

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_fs\_apply\_text</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Creates and returns a stream that will be used to replace

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_begin\_txn2
====================

Create a new transaction

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_fs\_begin\_txn2</span> ( <span
class="methodparam"><span class="type">resource</span> `$repos`</span> ,
<span class="methodparam"><span class="type">int</span> `$rev`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Create a new transaction

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_change\_node\_prop
===========================

Return true if everything is ok, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_change\_node\_prop</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> , <span class="methodparam"><span
class="type">string</span> `$name`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Return true if everything is ok, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_check\_path
====================

Determines what kind of item lives at path in a given repository fsroot

### 说明

<span class="type">int</span> <span
class="methodname">svn\_fs\_check\_path</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Determines what kind of item lives at path in a given repository fsroot

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_contents\_changed
==========================

Return true if content is different, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_contents\_changed</span> ( <span
class="methodparam"><span class="type">resource</span> `$root1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path1`</span> , <span class="methodparam"><span
class="type">resource</span> `$root2`</span> , <span
class="methodparam"><span class="type">string</span> `$path2`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Return true if content is different, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_copy
=============

Copies a file or a directory, returns true if all is ok, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_copy</span> ( <span
class="methodparam"><span class="type">resource</span>
`$from_root`</span> , <span class="methodparam"><span
class="type">string</span> `$from_path`</span> , <span
class="methodparam"><span class="type">resource</span> `$to_root`</span>
, <span class="methodparam"><span class="type">string</span>
`$to_path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Copies a file or a directory, returns true if all is ok, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_delete
===============

Deletes a file or a directory, return true if all is ok, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_delete</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Deletes a file or a directory, return true if all is ok, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_dir\_entries
=====================

Enumerates the directory entries under path; returns a hash of dir names
to file type

### 说明

<span class="type">array</span> <span
class="methodname">svn\_fs\_dir\_entries</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Enumerates the directory entries under path; returns a hash of dir names
to file type

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_file\_contents
=======================

Returns a stream to access the contents of a file from a given version
of the fs

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_fs\_file\_contents</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns a stream to access the contents of a file from a given version
of the fs

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_file\_length
=====================

Returns the length of a file from a given version of the fs

### 说明

<span class="type">int</span> <span
class="methodname">svn\_fs\_file\_length</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns the length of a file from a given version of the fs

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_is\_dir
================

Return true if the path points to a directory, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_is\_dir</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Return true if the path points to a directory, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_is\_file
=================

Return true if the path points to a file, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_is\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Return true if the path points to a file, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_make\_dir
==================

Creates a new empty directory, returns true if all is ok, false
otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_make\_dir</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Creates a new empty directory, returns true if all is ok, false
otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_make\_file
===================

Creates a new empty file, returns true if all is ok, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_make\_file</span> ( <span
class="methodparam"><span class="type">resource</span> `$root`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Creates a new empty file, returns true if all is ok, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_node\_created\_rev
===========================

Returns the revision in which path under fsroot was created

### 说明

<span class="type">int</span> <span
class="methodname">svn\_fs\_node\_created\_rev</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns the revision in which path under fsroot was created

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_node\_prop
===================

Returns the value of a property for a node

### 说明

<span class="type">string</span> <span
class="methodname">svn\_fs\_node\_prop</span> ( <span
class="methodparam"><span class="type">resource</span> `$fsroot`</span>
, <span class="methodparam"><span class="type">string</span>
`$path`</span> , <span class="methodparam"><span
class="type">string</span> `$propname`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns the value of a property for a node

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_props\_changed
=======================

Return true if props are different, false otherwise

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_fs\_props\_changed</span> ( <span
class="methodparam"><span class="type">resource</span> `$root1`</span> ,
<span class="methodparam"><span class="type">string</span>
`$path1`</span> , <span class="methodparam"><span
class="type">resource</span> `$root2`</span> , <span
class="methodparam"><span class="type">string</span> `$path2`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Return true if props are different, false otherwise

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_revision\_prop
=======================

Fetches the value of a named property

### 说明

<span class="type">string</span> <span
class="methodname">svn\_fs\_revision\_prop</span> ( <span
class="methodparam"><span class="type">resource</span> `$fs`</span> ,
<span class="methodparam"><span class="type">int</span> `$revnum`</span>
, <span class="methodparam"><span class="type">string</span>
`$propname`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Fetches the value of a named property

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_revision\_root
=======================

Get a handle on a specific version of the repository root

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_fs\_revision\_root</span> ( <span
class="methodparam"><span class="type">resource</span> `$fs`</span> ,
<span class="methodparam"><span class="type">int</span> `$revnum`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

Get a handle on a specific version of the repository root

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_txn\_root
==================

Creates and returns a transaction root

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_fs\_txn\_root</span> ( <span
class="methodparam"><span class="type">resource</span> `$txn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Creates and returns a transaction root

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_fs\_youngest\_rev
======================

Returns the number of the youngest revision in the filesystem

### 说明

<span class="type">int</span> <span
class="methodname">svn\_fs\_youngest\_rev</span> ( <span
class="methodparam"><span class="type">resource</span> `$fs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Returns the number of the youngest revision in the filesystem

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_import
===========

Imports an unversioned path into a repository

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_import</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> , <span
class="methodparam"><span class="type">string</span> `$url`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$nonrecursive`</span> )

Commits unversioned `path` into repository at `url`. If `path` is a
directory and `nonrecursive` is **`FALSE`**, the directory will be
imported recursively.

### 参数

`path`  
Path of file or directory to import.

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`url`  
Repository URL to import into.

`nonrecursive`  
Whether or not to refrain from recursively processing directories.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates a basic use-case of this function. To import a
directory named new-files into the repository at
http://www.example.com/svnroot/incoming/abc, use:

``` php
<?php
svn_import(realpath('new-files'), 'http://www.example.com/svnroot/incoming/abc', false);
?>
```

### 参见

-   <span class="function">svn\_add</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.import.html" class="link external">» SVN documentation for svn import</a>

svn\_log
========

Returns the commit log messages of a repository URL

### 说明

<span class="type">array</span> <span class="methodname">svn\_log</span>
( <span class="methodparam"><span class="type">string</span>
`$repos_url`</span> \[, <span class="methodparam"><span
class="type">int</span> `$start_revision`</span> \[, <span
class="methodparam"><span class="type">int</span> `$end_revision`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$limit`<span class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = SVN\_DISCOVER\_CHANGED\_PATHS \|
SVN\_STOP\_ON\_COPY</span></span> \]\]\]\] )

<span class="function">svn\_log</span> returns the complete history of
the item at the repository URL `repos_url`, or the history of a specific
revision if `start_revision` is set. This function is equivalent to
**`svn log --verbose -r $start_revision $repos_url`**.

### 参数

`repos_url`  
Repository URL of the item to retrieve log history from.

`start_revision`  
Revision number of the first log to retrieve. Use
**`SVN_REVISION_HEAD`** to retrieve the log from the most recent
revision.

`end_revision`  
Revision number of the last log to retrieve. Defaults to
`start_revision` if specified or to **`SVN_REVISION_INITIAL`**
otherwise.

`limit`  
Number of logs to retrieve.

`flags`  
Any combination of **`SVN_OMIT_MESSAGES`**,
**`SVN_DISCOVER_CHANGED_PATHS`** and **`SVN_STOP_ON_COPY`**.

### 返回值

On success, this function returns an array file listing in the format
of:

``` returnvalues
[0] => Array, ordered most recent (highest) revision first
(
    [rev] => integer revision number
    [author] => string author name
    [msg] => string log message
    [date] => string date formatted per ISO 8601, i.e. date('c')
    [paths] => Array, describing changed files
        (
            [0] => Array
                (
                    [action] => string letter signifying change
                    [path] =>  absolute repository path of changed file
                )
            [1] => ...
        )
)
[1] => ...
```

> **Note**:
>
> The output will always be a numerically indexed array of arrays, even
> when there are none or only one log message(s).

The value of `action` is a subset of the
<a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.status.html" class="link external">» status output in the first column</a>,
where possible values are:

| Letter | Description             |
|--------|-------------------------|
| M      | Item/props was modified |
| A      | Item was added          |
| D      | Item was deleted        |
| R      | Item was replaced       |

If no changes were made to the item, an empty array is returned.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 <span class="function">svn\_log</span> example**

``` php
<?php
print_r( svn_log('http://www.example.com/', 23) );
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
        (
            [rev] => 23
            [author] => 'joe'
            [msg] => 'Add cheese and salami to our sandwich.'
            [date] => '2007-04-06T16:00:27-04:00'
            [paths] => Array
                (
                    [0] => Array
                        (
                            [action] => 'M'
                            [path] =>  '/sandwich.txt'
                        )
                )
        )
    )

### 参见

-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.log.html" class="link external">»  SVN documentation on svn log</a>

svn\_ls
=======

Returns list of directory contents in repository URL, optionally at
revision number

### 说明

<span class="type">array</span> <span class="methodname">svn\_ls</span>
( <span class="methodparam"><span class="type">string</span>
`$repos_url`</span> \[, <span class="methodparam"><span
class="type">int</span> `$revision_no`<span class="initializer"> =
SVN\_REVISION\_HEAD</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$recurse`<span class="initializer"> =
**`FALSE`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$peg`<span class="initializer"> =
**`FALSE`**</span></span> \]\]\] )

This function queries the repository URL and returns a list of files and
directories, optionally from a specific revision. This is equivalent to
**`svn list $repos_url[@$revision_no]`**

> **Note**:
>
> This function does not work with working copies. `repos_url` *must* be
> a repository URL.

### 参数

`url`  
URL of the repository, eg. **`http://www.example.com/svnroot`**. To
access a local Subversion repository via filesystem, use the file URI
scheme, eg. **`file:///home/user/svn-repos`**

`revision`  
Integer revision number to retrieve listing of. When omitted, the HEAD
revision is used.

`recurse`  
Enables recursion.

### 返回值

On success, this function returns an array file listing in the format
of:

``` returnvalues
[0] => Array
    (
        [created_rev] => integer revision number of last edit
        [last_author] => string author name of last edit
        [size] => integer byte file size of file
        [time] => string date of last edit in form 'M d H:i'
                  or 'M d Y', depending on how old the file is
        [time_t] => integer unix timestamp of last edit
        [name] => name of file/directory
        [type] => type, can be 'file' or 'dir'
    )
[1] => ...
```

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 <span class="function">svn\_ls</span> example**

``` php
<?php
print_r( svn_ls('http://www.example.com/svnroot/') );
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [created_rev] => 20
                [last_author] => Joe
                [size] => 0
                [time] => Apr 02 09:28
                [time_t] => 1175520529
                [name] => tags
                [type] => dir
            )
        [1] => Array
            (
                [created_rev] => 23
                [last_author] => Bob
                [size] => 0
                [time] => Apr 02 15:15
                [time_t] => 1175541322
                [name] => trunk
                [type] => dir
            )
    )

### 参见

-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.list.html" class="link external">» SVN documentation on svn list</a>

svn\_mkdir
==========

Creates a directory in a working copy or repository

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_mkdir</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$log_message`</span> \] )

Creates a directory in a working copy or repository.

### 参数

`path`  
The path to the working copy or repository.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">svn\_add</span>
-   <span class="function">svn\_copy</span>

svn\_repos\_create
==================

Create a new subversion repository at path

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_repos\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$config`</span> \[, <span class="methodparam"><span
class="type">array</span> `$fsconfig`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

Create a new subversion repository at path

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_fs\_begin\_txn\_for\_commit
=======================================

Create a new transaction

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_repos\_fs\_begin\_txn\_for\_commit</span> (
<span class="methodparam"><span class="type">resource</span>
`$repos`</span> , <span class="methodparam"><span
class="type">int</span> `$rev`</span> , <span class="methodparam"><span
class="type">string</span> `$author`</span> , <span
class="methodparam"><span class="type">string</span> `$log_msg`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Create a new transaction

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_fs\_commit\_txn
===========================

Commits a transaction and returns the new revision

### 说明

<span class="type">int</span> <span
class="methodname">svn\_repos\_fs\_commit\_txn</span> ( <span
class="methodparam"><span class="type">resource</span> `$txn`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Commits a transaction and returns the new revision

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_fs
==============

Gets a handle on the filesystem for a repository

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_repos\_fs</span> ( <span
class="methodparam"><span class="type">resource</span> `$repos`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Gets a handle on the filesystem for a repository

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_hotcopy
===================

Make a hot-copy of the repos at repospath; copy it to destpath

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_repos\_hotcopy</span> ( <span
class="methodparam"><span class="type">string</span> `$repospath`</span>
, <span class="methodparam"><span class="type">string</span>
`$destpath`</span> , <span class="methodparam"><span
class="type">bool</span> `$cleanlogs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Make a hot-copy of the repos at repospath; copy it to destpath

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_open
================

Open a shared lock on a repository

### 说明

<span class="type">resource</span> <span
class="methodname">svn\_repos\_open</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Open a shared lock on a repository.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_repos\_recover
===================

Run recovery procedures on the repository located at path

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_repos\_recover</span> ( <span
class="methodparam"><span class="type">string</span> `$path`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

Run recovery procedures on the repository located at path.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

svn\_revert
===========

Revert changes to the working copy

### 说明

<span class="type">bool</span> <span
class="methodname">svn\_revert</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$recursive`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Revert any local changes to the path in a working copy.

### 参数

`path`  
The path to the working repository.

`recursive`  
Optionally make recursive changes.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 参见

-   <span class="function">svn\_delete</span>
-   <span class="function">svn\_export</span>

svn\_status
===========

Returns the status of working copy files and directories

### 说明

<span class="type">array</span> <span
class="methodname">svn\_status</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

Returns the status of working copy files and directories, giving
modifications, additions, deletions and other changes to items in the
working copy.

### 参数

`path`  
Local path to file or directory to retrieve status of.

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`flags`  
Any combination of **`Svn::NON_RECURSIVE`**, **`Svn::ALL`** (regardless
of modification status), **`Svn::SHOW_UPDATES`** (entries will be added
for items that are out-of-date), **`Svn::NO_IGNORE`** (disregard
*svn:ignore* properties when scanning for new files) and
**`Svn::IGNORE_EXTERNALS`**.

### 返回值

Returns a numerically indexed array of associative arrays detailing the
status of items in the repository:

``` returnvalues
Array (
    [0] => Array (
        // information on item
    )
    [1] => ...
)
```

The information on the item is an associative array that can contain the
following keys:

`path`  
<span class="simpara"> String path to file/directory of this entry on
local filesystem. </span>

`text_status`  
<span class="simpara"> Status of item's text. 参见
<a href="/svn/constants.html#Working%20copy%20status%20constants" class="link">状态常量列表</a>
获得可能的值. </span>

`repos_text_status`  
<span class="simpara"> Status of item's text in repository. Only
accurate if `update` was set to **`TRUE`**. 参见
<a href="/svn/constants.html#Working%20copy%20status%20constants" class="link">状态常量列表</a>
获得可能的值. </span>

`prop_status`  
<span class="simpara"> Status of item's properties. 参见
<a href="/svn/constants.html#Working%20copy%20status%20constants" class="link">状态常量列表</a>
获得可能的值. </span>

`repos_prop_status`  
<span class="simpara"> Status of item's property in repository. Only
accurate if `update` was set to **`TRUE`**. 参见
<a href="/svn/constants.html#Working%20copy%20status%20constants" class="link">状态常量列表</a>
获得可能的值. </span>

`locked`  
<span class="simpara"> Whether or not the item is locked. (Only set if
**`TRUE`**.) </span>

`copied`  
<span class="simpara"> Whether or not the item was copied (scheduled for
addition with history). (Only set if **`TRUE`**.) </span>

`switched`  
<span class="simpara"> Whether or not the item was switched using the
switch command. (Only set if **`TRUE`**) </span>

These keys are only set if the item is versioned:

`name`  
<span class="simpara"> Base name of item in repository. </span>

`url`  
<span class="simpara"> URL of item in repository. </span>

`repos`  
<span class="simpara"> Base URL of repository. </span>

`revision`  
<span class="simpara"> Integer revision of item in working copy. </span>

`kind`  
<span class="simpara"> Type of item, i.e. file or directory. 参见
<a href="/svn/constants.html#Node%20type%20constants" class="link">类型常量列表</a>
获取可能的值. </span>

`schedule`  
<span class="simpara"> Scheduled action for item, i.e. addition or
deletion. Constants for these magic numbers are not available, they can
be emulated by using: </span>

``` php
<?php
if (!defined('svn_wc_schedule_normal')) {
    define('svn_wc_schedule_normal',  0); // nothing special
    define('svn_wc_schedule_add',     1); // item will be added
    define('svn_wc_schedule_delete',  2); // item will be deleted
    define('svn_wc_schedule_replace', 3); // item will be added and deleted
}
?>
```

`deleted`  
<span class="simpara"> Whether or not the item was deleted, but parent
revision lags behind. (Only set if **`TRUE`**.) </span>

`absent`  
<span class="simpara"> Whether or not the item is absent, that is,
Subversion knows that there should be something there but there isn't.
(Only set if **`TRUE`**.) </span>

`incomplete`  
<span class="simpara"> Whether or not the entries file for a directory
is incomplete. (Only set if **`TRUE`**.) </span>

`cmt_date`  
<span class="simpara"> Integer Unix timestamp of last commit date.
(Unaffected by `update`.) </span>

`cmt_rev`  
<span class="simpara"> Integer revision of last commit. (Unaffected by
`update`.) </span>

`cmt_author`  
<span class="simpara"> String author of last commit. (Unaffected by
`update`.) </span>

`prop_time`  
<span class="simpara"> Integer Unix timestamp of last up-to-date time
for properties </span>

`text_time`  
<span class="simpara"> Integer Unix timestamp of last up-to-date time
for text </span>

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates a basic, theoretical usage of this function.

``` php
<?php
print_r(svn_status(realpath('wc')));
?>
```

以上例程的输出类似于：

    Array (
        [0] => Array (
            [path] => /home/bob/wc/sandwich.txt
            [text_status] => 8 // item was modified
            [repos_text_status] => 1 // no information available, use update
            [prop_status] => 3 // no changes
            [repos_prop_status] => 1 // no information available, use update
            [name] => sandwich.txt
            [url] => http://www.example.com/svnroot/deli/trunk/sandwich.txt
            [repos] => http://www.example.com/svnroot/
            [revision] => 123
            [kind] => 1 // file
            [schedule] => 0 // no special actions scheduled
            [cmt_date] => 1165543135
            [cmt_rev] => 120
            [cmt_author] => Alice
            [prop_time] => 1180201728
            [text_time] => 1180201729
        )
    )

### 参见

-   <span class="function">svn\_update</span>
-   <span class="function">svn\_log</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.status.html" class="link external">» SVN documentation for svn status</a>

svn\_update
===========

Update working copy

### 说明

<span class="type">int</span> <span
class="methodname">svn\_update</span> ( <span class="methodparam"><span
class="type">string</span> `$path`</span> \[, <span
class="methodparam"><span class="type">int</span> `$revno`<span
class="initializer"> = SVN\_REVISION\_HEAD</span></span> \[, <span
class="methodparam"><span class="type">bool</span> `$recurse`<span
class="initializer"> = **`TRUE`**</span></span> \]\] )

Update working copy at `path` to revision `revno`. If `recurse` is true,
directories will be recursively updated.

### 参数

`path`  
Path to local working copy.

> **Note**: <span
> class="simpara">相对路径将会以PHP执行文件所在目录作为当前工作目录进行解析。如果希望依据脚本所在目录解析,
> 使用<span class="function">realpath</span> 或
> dirname(\_\_FILE\_\_)。</span>

`revno`  
Revision number to update to, default is **`SVN_REVISION_HEAD`**.

`recurse`  
Whether or not to recursively update directories.

### 返回值

Returns new revision number on success, returns **`FALSE`** on failure.

### 注释

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

### 范例

**示例 \#1 Basic example**

This example demonstrates basic usage of this function:

``` php
<?php
echo svn_update(realpath('working-copy'));
?>
```

以上例程的输出类似于：

    234

### 参见

-   <span class="function">svn\_checkout</span>
-   <span class="function">svn\_commit</span>
-   <a href="http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.update.html" class="link external">» SVN documentation for svn update</a>

**目录**

-   [svn\_add](/ref/svn.html#svn_add) — 计划在工作目录添加项
-   [svn\_auth\_get\_parameter](/ref/svn.html#svn_auth_get_parameter) —
    Retrieves authentication parameter
-   [svn\_auth\_set\_parameter](/ref/svn.html#svn_auth_set_parameter) —
    Sets an authentication parameter
-   [svn\_blame](/ref/svn.html#svn_blame) — Get the SVN blame for a file
-   [svn\_cat](/ref/svn.html#svn_cat) — Returns the contents of a file
    in a repository
-   [svn\_checkout](/ref/svn.html#svn_checkout) — Checks out a working
    copy from the repository
-   [svn\_cleanup](/ref/svn.html#svn_cleanup) — Recursively cleanup a
    working copy directory, finishing incomplete operations and removing
    locks
-   [svn\_client\_version](/ref/svn.html#svn_client_version) — Returns
    the version of the SVN client libraries
-   [svn\_commit](/ref/svn.html#svn_commit) —
    将修改的本地文件副本发送至版本库
-   [svn\_delete](/ref/svn.html#svn_delete) — Delete items from a
    working copy or repository
-   [svn\_diff](/ref/svn.html#svn_diff) — Recursively diffs two paths
-   [svn\_export](/ref/svn.html#svn_export) — Export the contents of a
    SVN directory
-   [svn\_fs\_abort\_txn](/ref/svn.html#svn_fs_abort_txn) — Abort a
    transaction, returns true if everything is okay, false otherwise
-   [svn\_fs\_apply\_text](/ref/svn.html#svn_fs_apply_text) — Creates
    and returns a stream that will be used to replace
-   [svn\_fs\_begin\_txn2](/ref/svn.html#svn_fs_begin_txn2) — Create a
    new transaction
-   [svn\_fs\_change\_node\_prop](/ref/svn.html#svn_fs_change_node_prop)
    — Return true if everything is ok, false otherwise
-   [svn\_fs\_check\_path](/ref/svn.html#svn_fs_check_path) — Determines
    what kind of item lives at path in a given repository fsroot
-   [svn\_fs\_contents\_changed](/ref/svn.html#svn_fs_contents_changed)
    — Return true if content is different, false otherwise
-   [svn\_fs\_copy](/ref/svn.html#svn_fs_copy) — Copies a file or a
    directory, returns true if all is ok, false otherwise
-   [svn\_fs\_delete](/ref/svn.html#svn_fs_delete) — Deletes a file or a
    directory, return true if all is ok, false otherwise
-   [svn\_fs\_dir\_entries](/ref/svn.html#svn_fs_dir_entries) —
    Enumerates the directory entries under path; returns a hash of dir
    names to file type
-   [svn\_fs\_file\_contents](/ref/svn.html#svn_fs_file_contents) —
    Returns a stream to access the contents of a file from a given
    version of the fs
-   [svn\_fs\_file\_length](/ref/svn.html#svn_fs_file_length) — Returns
    the length of a file from a given version of the fs
-   [svn\_fs\_is\_dir](/ref/svn.html#svn_fs_is_dir) — Return true if the
    path points to a directory, false otherwise
-   [svn\_fs\_is\_file](/ref/svn.html#svn_fs_is_file) — Return true if
    the path points to a file, false otherwise
-   [svn\_fs\_make\_dir](/ref/svn.html#svn_fs_make_dir) — Creates a new
    empty directory, returns true if all is ok, false otherwise
-   [svn\_fs\_make\_file](/ref/svn.html#svn_fs_make_file) — Creates a
    new empty file, returns true if all is ok, false otherwise
-   [svn\_fs\_node\_created\_rev](/ref/svn.html#svn_fs_node_created_rev)
    — Returns the revision in which path under fsroot was created
-   [svn\_fs\_node\_prop](/ref/svn.html#svn_fs_node_prop) — Returns the
    value of a property for a node
-   [svn\_fs\_props\_changed](/ref/svn.html#svn_fs_props_changed) —
    Return true if props are different, false otherwise
-   [svn\_fs\_revision\_prop](/ref/svn.html#svn_fs_revision_prop) —
    Fetches the value of a named property
-   [svn\_fs\_revision\_root](/ref/svn.html#svn_fs_revision_root) — Get
    a handle on a specific version of the repository root
-   [svn\_fs\_txn\_root](/ref/svn.html#svn_fs_txn_root) — Creates and
    returns a transaction root
-   [svn\_fs\_youngest\_rev](/ref/svn.html#svn_fs_youngest_rev) —
    Returns the number of the youngest revision in the filesystem
-   [svn\_import](/ref/svn.html#svn_import) — Imports an unversioned
    path into a repository
-   [svn\_log](/ref/svn.html#svn_log) — Returns the commit log messages
    of a repository URL
-   [svn\_ls](/ref/svn.html#svn_ls) — Returns list of directory contents
    in repository URL, optionally at revision number
-   [svn\_mkdir](/ref/svn.html#svn_mkdir) — Creates a directory in a
    working copy or repository
-   [svn\_repos\_create](/ref/svn.html#svn_repos_create) — Create a new
    subversion repository at path
-   [svn\_repos\_fs\_begin\_txn\_for\_commit](/ref/svn.html#svn_repos_fs_begin_txn_for_commit)
    — Create a new transaction
-   [svn\_repos\_fs\_commit\_txn](/ref/svn.html#svn_repos_fs_commit_txn)
    — Commits a transaction and returns the new revision
-   [svn\_repos\_fs](/ref/svn.html#svn_repos_fs) — Gets a handle on the
    filesystem for a repository
-   [svn\_repos\_hotcopy](/ref/svn.html#svn_repos_hotcopy) — Make a
    hot-copy of the repos at repospath; copy it to destpath
-   [svn\_repos\_open](/ref/svn.html#svn_repos_open) — Open a shared
    lock on a repository
-   [svn\_repos\_recover](/ref/svn.html#svn_repos_recover) — Run
    recovery procedures on the repository located at path
-   [svn\_revert](/ref/svn.html#svn_revert) — Revert changes to the
    working copy
-   [svn\_status](/ref/svn.html#svn_status) — Returns the status of
    working copy files and directories
-   [svn\_update](/ref/svn.html#svn_update) — Update working copy
