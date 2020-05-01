**Warning**

This extension is *DEPRECATED* and *UNBUNDLED* as of PHP 7.4.0.

These functions are intended for work with
<a href="http://www.openwddx.org/" class="link external">» WDDX</a>.

**Warning**

Do not pass untrusted user input to <span
class="function">wddx\_deserialize</span>. Unserialization can result in
code being loaded and executed due to object instantiation and
autoloading, and a malicious user may be able to exploit this. Use a
safe, standard data interchange format such as JSON (via <span
class="function">json\_decode</span> and <span
class="function">json\_encode</span>) if you need to pass serialized
data to the user.
