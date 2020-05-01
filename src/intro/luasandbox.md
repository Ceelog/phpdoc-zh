LuaSandbox is an extension for PHP 5, PHP 7, and HHVM to allow safely
running untrusted Lua 5.1 code from within PHP.

Differences compared to the
<a href="/book/lua.html" class="link">Lua</a> extension:

-   LuaSandbox has support for time and memory limits.

-   LuaSandbox provides a default-safe environment for running untrusted
    code. Stock Lua functions were reviewed for security, and several
    were patched accordingly.

-   LuaSandbox has a PHP interface which is more complex, precise and
    powerful, but it is less convenient for developers.

-   LuaSandbox supports only Lua 5.1. It is difficult to change this,
    because LuaSandbox uses heavily modified Lua standard libraries, and
    due to the lack of backwards compatibility between major Lua
    versions. LuaSandbox aims to maximise backwards compatibility with
    user-supplied scripts.
