范例
====

This example shows how to open a CrackLib dictionary, test a given
password, retrieve any diagnostic messages, and close the dictionary.

**示例 \#1 CrackLib example**

``` php
<?php
// Open CrackLib Dictionary
$dictionary = crack_opendict('/usr/local/lib/pw_dict')
     or die('Unable to open CrackLib dictionary');

// Perform password check
$check = crack_check($dictionary, 'gx9A2s0x');

// Retrieve messages
$diag = crack_getlastmessage();
echo $diag; // 'strong password'

// Close dictionary
crack_closedict($dictionary);
?>
```

> **Note**:
>
> If <span class="function">crack\_check</span> returns **`TRUE`**,
> <span class="function">crack\_getlastmessage</span> will return
> *'strong password'*.
