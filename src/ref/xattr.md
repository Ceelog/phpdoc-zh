xattr\_get
==========

Get an extended attribute

### 说明

<span class="type"><span class="type">string</span><span
class="type">false</span></span> <span
class="methodname">xattr\_get</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

This function gets the value of an extended attribute of a file.

扩展的属性有两种 不同的命名空间：user 和 root。user
命名空间对所有用户均有效，而 root 命名空间仅对拥有 root 权限的用户有效。
xattr 默认在 user 命名空间上操作，但可使用 `flags` 参数进行更改。

### 参数

`filename`  
The file from which we get the attribute.

`name`  
The name of the attribute.

`flags`  
|                        |                                                                      |
|------------------------|----------------------------------------------------------------------|
| **`XATTR_DONTFOLLOW`** | Do not follow the symbolic link but operate on symbolic link itself. |
| **`XATTR_ROOT`**       | Set attribute in root (trusted) namespace. Requires root privileges. |

### 返回值

Returns a string containing the value or **`FALSE`** if the attribute
doesn't exist.

### 范例

**示例 \#1 Checks if system administrator has signed the file**

``` php
<?php
$file = '/usr/local/sbin/some_binary';
$signature = xattr_get($file, 'Root signature', XATTR_ROOT);

/* ... check if $signature is valid ... */

?>
```

### 参见

-   <span class="function">xattr\_list</span>
-   <span class="function">xattr\_set</span>
-   <span class="function">xattr\_remove</span>

xattr\_list
===========

Get a list of extended attributes

### 说明

<span class="type">array</span> <span
class="methodname">xattr\_list</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \] )

This functions gets a list of names of extended attributes of a file.

扩展的属性有两种 不同的命名空间：user 和 root。user
命名空间对所有用户均有效，而 root 命名空间仅对拥有 root 权限的用户有效。
xattr 默认在 user 命名空间上操作，但可使用 `flags` 参数进行更改。

### 参数

`filename`  
The path of the file.

`flags`  
|                        |                                                                      |
|------------------------|----------------------------------------------------------------------|
| **`XATTR_DONTFOLLOW`** | Do not follow the symbolic link but operate on symbolic link itself. |
| **`XATTR_ROOT`**       | Set attribute in root (trusted) namespace. Requires root privileges. |

### 返回值

This function returns an array with names of extended attributes.

### 范例

**示例 \#1 Prints names of all extended attributes of file**

``` php
<?php
$file = 'some_file';
$root_attributes = xattr_list($file, XATTR_ROOT);
$user_attributes = xattr_list($file);

echo "Root attributes: \n";
foreach ($root_attributes as $attr_name) {
    printf("%s\n", $attr_name);
}

echo "\n User attributes: \n";
foreach ($attributes as $attr_name) {
    printf("%s\n", $attr_name);
}

?>
```

### 参见

-   <span class="function">xattr\_get</span>

xattr\_remove
=============

Remove an extended attribute

### 说明

<span class="type">bool</span> <span
class="methodname">xattr\_remove</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
, <span class="methodparam"><span class="type">string</span>
`$name`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

This function removes an extended attribute of a file.

扩展的属性有两种 不同的命名空间：user 和 root。user
命名空间对所有用户均有效，而 root 命名空间仅对拥有 root 权限的用户有效。
xattr 默认在 user 命名空间上操作，但可使用 `flags` 参数进行更改。

### 参数

`filename`  
The file from which we remove the attribute.

`name`  
The name of the attribute to remove.

`flags`  
|                        |                                                                      |
|------------------------|----------------------------------------------------------------------|
| **`XATTR_DONTFOLLOW`** | Do not follow the symbolic link but operate on symbolic link itself. |
| **`XATTR_ROOT`**       | Set attribute in root (trusted) namespace. Requires root privileges. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Removes all extended attributes of a file**

``` php
<?php
$file = 'some_file';
$attributes = xattr_list($file);

foreach ($attributes as $attr_name) {
    xattr_remove($file, $attr_name);
}
?>
```

### 参见

-   <span class="function">xattr\_list</span>
-   <span class="function">xattr\_set</span>
-   <span class="function">xattr\_get</span>

xattr\_set
==========

Set an extended attribute

### 说明

<span class="type">bool</span> <span
class="methodname">xattr\_set</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> , <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`<span class="initializer"> =
0</span></span> \] )

This function sets the value of an extended attribute of a file.

扩展的属性有两种 不同的命名空间：user 和 root。user
命名空间对所有用户均有效，而 root 命名空间仅对拥有 root 权限的用户有效。
xattr 默认在 user 命名空间上操作，但可使用 `flags` 参数进行更改。

### 参数

`filename`  
The file in which we set the attribute.

`name`  
The name of the extended attribute. This attribute will be created if it
doesn't exist or replaced otherwise. You can change this behaviour by
using the `flags` parameter.

`value`  
The value of the attribute.

`flags`  
|                        |                                                                      |
|------------------------|----------------------------------------------------------------------|
| **`XATTR_CREATE`**     | Function will fail if extended attribute already exists.             |
| **`XATTR_REPLACE`**    | Function will fail if extended attribute doesn't exist.              |
| **`XATTR_DONTFOLLOW`** | Do not follow the symbolic link but operate on symbolic link itself. |
| **`XATTR_ROOT`**       | Set attribute in root (trusted) namespace. Requires root privileges. |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Sets extended attributes on `.wav` file**

``` php
<?php
$file = 'my_favourite_song.wav';
xattr_set($file, 'Artist', 'Someone');
xattr_set($file, 'My ranking', 'Good');
xattr_set($file, 'Listen count', '34');

/* ... other code ... */

printf("You've played this song %d times", xattr_get($file, 'Listen count')); 
?>
```

### 参见

-   <span class="function">xattr\_get</span>
-   <span class="function">xattr\_remove</span>

xattr\_supported
================

Check if filesystem supports extended attributes

### 说明

<span class="type">bool</span> <span
class="methodname">xattr\_supported</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`<span class="initializer"> = 0</span></span> \] )

This functions checks if the filesystem holding the given file supports
extended attributes. Read access to the file is required.

### 参数

`filename`  
The path of the tested file.

`flags`  
|                        |                                                                      |
|------------------------|----------------------------------------------------------------------|
| **`XATTR_DONTFOLLOW`** | Do not follow the symbolic link but operate on symbolic link itself. |

### 返回值

This function returns **`TRUE`** if filesystem supports extended
attributes, **`FALSE`** if it doesn't and **`NULL`** if it can't be
determined (for example wrong path or lack of permissions to file).

### 范例

**示例 \#1 <span class="function">xattr\_supported</span> example**

The following code checks if we can use extended attributes.

``` php
<?php
$file = 'some_file';

if (xattr_supported($file)) {
    /* ... make use of some xattr_* functions ... */
}

?>
```

### 参见

-   <span class="function">xattr\_get</span>
-   <span class="function">xattr\_list</span>

**目录**

-   [xattr\_get](/ref/xattr.html#xattr_get) — Get an extended attribute
-   [xattr\_list](/ref/xattr.html#xattr_list) — Get a list of extended
    attributes
-   [xattr\_remove](/ref/xattr.html#xattr_remove) — Remove an extended
    attribute
-   [xattr\_set](/ref/xattr.html#xattr_set) — Set an extended attribute
-   [xattr\_supported](/ref/xattr.html#xattr_supported) — Check if
    filesystem supports extended attributes
