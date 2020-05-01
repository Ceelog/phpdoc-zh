Differences from Standard Lua
=============================

LuaSandbox provides a sandboxed environment which differs in some ways
from standard Lua 5.1.

-   *dofile()*, *loadfile()*, and the *io* package, as they allow direct
    filesystem access. If needed, filesystem access should be done via
    PHP callbacks.

-   The *package* package, including *require()* and *module()*, as it
    depends heavily on direct filesystem access. A pure-Lua rewrite such
    as that used in the MediaWiki Scribunto extension may be used
    instead.

-   *load()* and *loadstring()*, to allow for static analysis of Lua
    code.

-   *print()*, since it outputs to standard output. If needed, output
    should be done via PHP callbacks.

-   Most of the *os* package, as it allows manipulation of the process
    and executing of other processes.

    -   *os.clock()*, *os.date()*, *os.difftime()*, and *os.time()*
        remain available.

-   Most of the *debug* package, as it allows manipulation of Lua state
    and metadata in ways that can break sandboxing.

    -   *debug.traceback()* remains available.

-   *string.dump()*, as it may expose internal data.

-   *collectgarbage()*, *gcinfo()*, and the *coroutine* package have not
    been reviewed for security.

-   *pcall()* and *xpcall()* cannot catch certain errors, particularly
    timeout errors.

-   *tostring()* does not include pointer addresses.

-   *string.match()* has been patched to limit the recursion depth and
    to periodically check for a timeout.

-   *math.random()* and *math.randomseed()* are replaced with versions
    that don't share state with PHP's *rand()*.

-   The Lua 5.2 *\_\_pairs* and *\_\_ipairs* metamethods are supported
    by *pairs()* and *ipairs()*.
