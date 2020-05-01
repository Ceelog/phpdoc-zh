Extension globals
-----------------

### Introduction to globals in a PHP extension

In a language such as C, a "global" variable is a variable that can be
accessed from any function without any extra declaration. These
traditional globals have a few drawbacks:

-   <span class="simpara"> Barring any special options passed to the
    compiler, a global variable can be accessed and changed by any piece
    of code anywhere in the program, whether or not that code should be
    doing so. </span>
-   <span class="simpara"> A typical global variable is not thread safe.
    </span>
-   <span class="simpara"> The names of global variables are as global
    as the variables themselves. </span>

A PHP extension's globals are more properly called the "extension
state", since most modules must remember what they're doing between
function calls. The "counter" extension is a perfect example of this
need: The basic interface calls for a counter with a persistent value. A
programmer new to Zend and PHP might do something like this in
`counter.c` to store that value:

**示例 \#1 The wrong way to store the basic counter interface's value**

``` c
/* ... */
static long basic_counter_value;

/* ... */

PHP_FUNCTION(counter_get)
{
    RETURN_LONG(basic_counter_value);
}
```

On the surface this appears a viable solution, and indeed in a simple
test it would function correctly. However, there are a number of
situations in which more than one copy of PHP is running in the same
thread, which means more than one instance of the counter module.
Suddenly these multiple threads are sharing the same counter value,
which is clearly undesirable. Another problem shows itself when
considering that another extension might someday happen to have a global
with the same name, and due to the rules of C scoping, this has the
potential to cause a compile failure, or worse, a runtime error.
Something more elaborate is needed, and so exists Zend's support for
thread-safe per-module globals.

### Declaring module globals

Whether a module uses only a single global or dozens, they must be
defined in a structure, and that structure must be declared. There are
some macros that assist with doing so in a way that avoids name
conflicts between modules: <span
class="function">ZEND\_BEGIN\_MODULE\_GLOBALS</span>, <span
class="function">ZEND\_END\_MODULE\_GLOBALS</span>, and <span
class="function">ZEND\_DECLARE\_MODULE\_GLOBALS</span>. All three take
as a parameter the short name of the module, which in the case of the
counter module is simply *"counter"*. Here is the global structure
declaration from `php_counter.h`:

**示例 \#2 The counter module's globals**

``` c
ZEND_BEGIN_MODULE_GLOBALS(counter)
    long        basic_counter_value;
ZEND_END_MODULE_GLOBALS(counter)
```

And this is the declaration from `counter.c`:

**示例 \#3 The counter module's global structure declaration**

``` c
ZEND_DECLARE_MODULE_GLOBALS(counter)
```

### Accessing module globals

As discussed above, per-module globals are declared inside a C structure
whose name is obscured by Zend macros. As a result, the ideal way to
access members of this structure is by the use of further macros.
Accordingly, most if not all extensions which have globals have a
declaration like this somewhere in their header file:

**示例 \#4 Accessor macros for per-module globals**

``` c
#ifdef ZTS
#define COUNTER_G(v) TSRMG(counter_globals_id, zend_counter_globals *, v)
#else
#define COUNTER_G(v) (counter_globals.v)
#endif
```

> **Note**: <span class="simpara"> This could have been generalized into
> a macro of its own by the Zend API, but as of PHP 5.3 (and PHP 6 at
> the time of this writing), that hasn't happened. The global accessor
> construct is written into the header by **ext\_skel** and thus is
> generally left alone by extension writers, unless they wish to change
> the name of the accessor macro. </span>

> **Note**: <span class="simpara"> **`COUNTER_G`** was the name given to
> the macro by **ext\_skel**, but it's not necessary for it to have that
> name and could just as easily be called *FOO* instead. </span>

Any code in the counter extension that accesses a global must thus wrap
it in the macro **`COUNTER_G`**.

**Warning**

Any function which accesses globals must either be declared by Zend
macros, have **`TSRMLS_DC`** as its last argument, or call the macro
**`TSRMLS_FETCH`** before accessing the globals. See the TSRM
documentation for more information.

So with all of that in mind, here is our new version of the <span
class="function">counter\_get</span>:

**示例 \#5 The right way to store the basic counter interface's value**

``` c
/* php_counter.h */
ZEND_BEGIN_MODULE_GLOBALS(counter)
    long        basic_counter_value;
ZEND_END_MODULE_GLOBALS(counter)

#ifdef ZTS
#define COUNTER_G(v) TSRMG(counter_globals_id, zend_counter_globals *, v)
#else
#define COUNTER_G(v) (counter_globals.v)
#endif

/* counter.c */
ZEND_DECLARE_MODULE_GLOBALS(counter)

/* ... */

PHP_FUNCTION(counter_get)
{
    RETURN_LONG(COUNTER_G(basic_counter_value));
}
```

This is a correct implementation. It is not, however, a complete one.
The section
<a href="/internals2/structure/lifecycle.html" class="xref">Life cycle of an extension</a>
explains why.
