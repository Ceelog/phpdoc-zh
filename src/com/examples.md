范例
====

**目录**

-   [For Each](/com/examples.html#For%20Each)
-   [Arrays and Array-style COM
    properties](/com/examples.html#Arrays%20and%20Array-style%20COM%20properties)

For Each
--------

You may use PHP's own
<a href="/control-structures/foreach.html" class="link">foreach</a>
statement to iterate over the contents of a standard COM/OLE
IEnumVariant. In layman's terms, this means that you can use foreach in
places where you would have used *For Each* in VB/ASP code.

**示例 \#1 For Each in ASP**

``` asp
<%
Set domainObject = GetObject("WinNT://Domain")
For Each obj in domainObject
  Response.Write obj.Name & "<br />"
Next
%>
```

**示例 \#2 foreach in PHP**

``` php
<?php 
$domainObject = new COM("WinNT://Domain"); 
foreach ($domainObject as $obj) { 
   echo $obj->Name . "<br />"; 
} 
?>
```

Arrays and Array-style COM properties
-------------------------------------

Many COM objects expose their properties as arrays, or using array-style
access.

You can:

-   Access multi-dimensional arrays, or COM properties that require
    multiple parameters using PHP array syntax. You can also write or
    set properties using this technique.

-   Iterate SafeArrays ("true" arrays) using the
    <a href="/control-structures/foreach.html" class="link">foreach</a>
    control structure. This works because SafeArrays include information
    about their size. If an array-style property implements IEnumVariant
    then you can also use foreach for that property too; take a look at
    <a href="/com/examples.html#For%20Each" class="xref"></a> for more
    information on this topic.
