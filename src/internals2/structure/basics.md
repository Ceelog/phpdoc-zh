Basic constructs
----------------

C is a very low-level language by modern definitions. This means that it
has no built-in support for many features that PHP takes for granted,
such as reflection, dynamic module loading, bounds checking, threadsafe
data management and various useful data structures including linked
lists and hash tables. At the same time, C is a common denominator of
language support and functionality. Given enough work, none of these
concepts are impossible; the Zend Engine uses them all.

A lot of effort has gone into making the Zend API both extensible and
understandable, but C forces certain necessary declarations upon any
extension that to an inexperienced eye seem redundant or plain
unnecessary. All of those constructs, detailed in this section, are
"write once and forget" in Zend Engine 2 and 3. Here are some excerpts
from the pre-generated `php_counter.h` and `counter.c` files created by
PHP 5.3's **ext\_skel**, showing the pre-generated declarations:

> **Note**: <span class="simpara"> The astute reader will notice that
> there are several declarations in the real files that aren't shown
> here. Those declarations are specific to various Zend subsystems and
> are discussed elsewhere as appropriate. </span>

    extern zend_module_entry counter_module_entry;
    #define phpext_counter_ptr &counter_module_entry

    #ifdef PHP_WIN32
    #    define PHP_COUNTER_API __declspec(dllexport)
    #elif defined(__GNUC__) && __GNUC__ >= 4
    #    define PHP_COUNTER_API __attribute__ ((visibility("default")))
    #else
    #    define PHP_COUNTER_API
    #endif

    #ifdef ZTS
    #include "TSRM.h"
    #endif

    #ifdef HAVE_CONFIG_H
    #include "config.h"
    #endif

    #include "php.h"
    #include "php_ini.h"
    #include "ext/standard/info.h"
    #include "php_counter.h"

    /* ... */

    #ifdef COMPILE_DL_COUNTER
    ZEND_GET_MODULE(counter)
    #endif

-   <span class="simpara"> The lines concerning *counter\_module\_entry*
    declare a global variable, and a macroed pointer to it, which
    contains the *zend\_module\_entry* for the extension. Despite the
    later discussion regarding the drawbacks of "true" globals, this
    usage is intentional; Zend takes precautions to avoid misusing this
    variable. </span>

-   <span class="simpara"> **`PHP_COUNTER_API`** is declared for use by
    non-PHP functions the module intends to export for the use of other
    modules. The counter extension doesn't declare any of these, and in
    the final version of the header file, this macro has been removed.
    The **`PHPAPI`** macro is declared identically elsewhere and is used
    by the standard extension to make the <span
    class="function">phpinfo</span> utility functions available to other
    extensions. </span>

-   <span class="simpara"> The include of `TSRM.h` is skipped if PHP, or
    the extension, isn't being compiled with thread-safety, since in
    that case TSRM isn't used. </span>

-   <span class="simpara"> A standard list of includes, especially the
    extension's own `php_counter.h`, is given. `config.h` gives the
    extension access to determinations made by **configure**. `php.h` is
    the gateway to the entire PHP and Zend APIs. `php_ini.h` adds the
    APIs for runtime configuration (INI) entries. Not all extensions
    will use this. Finally, `ext/standard/info.h` imports the
    aforementioned <span class="function">phpinfo</span> utility API.
    </span>

-   <span class="simpara"> **`COMPILE_DL_COUNTER`** will only be defined
    by **configure** if the counter extension is both enabled and wants
    to be built as a dynamically loadable module instead of being
    statically linked into PHP. **`ZEND_GET_MODULE`** defines a tiny
    function which Zend can use to get the extension's
    *zend\_module\_entry* at runtime. </span>

    > **Note**: <span class="simpara"> The astute reader who has peeked
    > into `main/php_config.h` after trying to build with the counter
    > module enabled statically may have noticed that there is also a
    > **`HAVE_COUNTER`** constant defined that the source code doesn't
    > check for. There's a simple reason this check isn't done: It's
    > unnecessary. If the extension isn't enabled, the source file will
    > never be compiled. </span>
