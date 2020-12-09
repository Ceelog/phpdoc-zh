Error Reporting
---------------

Some of the existing **`E_ERROR`** conditions have been converted to
something that can be caught with a user-defined error handler. If an
<a href="/errorfunc/constants.html" class="link"><strong><code>E_RECOVERABLE_ERROR</code></strong></a>
is not handled, it will behave in the same way as **`E_ERROR`** behaves
in all versions of PHP. Errors of this type are logged as *Catchable
fatal error*.

This change means that the value of the **`E_ALL`**
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a>
constant is now 6143, where the previous value was 2047. Because PHP
constants have no meaning outside of PHP, in some cases the integer
value is used instead so these will need to be adjusted. So for example
by setting the error\_reporting mode from either the
<a href="/apache/setup.html#运行时配置" class="link">httpd.conf</a> or
the `.htaccess` files, the value has to be changed accordingly. The same
applies when the numeric values are used rather than the constants in
PHP scripts.

As a side-effect of a change made to prevent duplicate error messages
when <a href="/errorfunc/setup.html#" class="link">track_errors</a> is
*On*, it is now necessary to return **`false`** from user defined error
handlers in order to populate `$php_errormsg`. This provides a
fine-grain control over the levels of messages stored.
