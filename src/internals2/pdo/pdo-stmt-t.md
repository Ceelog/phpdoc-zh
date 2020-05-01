pdo\_stmt\_t definition
-----------------------

All fields should be treated as read-only unless explicitly stated
otherwise.

``` c
/* represents a prepared statement */
struct _pdo_stmt_t {
    /* driver specifics */
    struct pdo_stmt_methods *methods;
```

<span id="internals2.pdo.stmt.co.methods">\*</span>

``` c
void *driver_data;
```

<span id="internals2.pdo.stmt.co.driver-data">\*\*</span>

``` c
/* if true, we've already successfully executed this statement at least
     * once */
    unsigned executed:1;
```

<span id="internals2.pdo.stmt.co.executed">\*\*\*</span>

``` c
/* if true, the statement supports placeholders and can implement
     * bindParam() for its prepared statements, if false, PDO should
     * emulate prepare and bind on its behalf */
    unsigned supports_placeholders:2;
```

<span id="internals2.pdo.stmt.co.holder">\*\*\*\*</span>

``` c
/* the number of columns in the result set; not valid until after
     * the statement has been executed at least once.  In some cases, might
     * not be valid until fetch (at the driver level) has been called at least once.
     * */
    int column_count;
```

<span id="internals2.pdo.stmt.co.colcount">\*\*\*\*\*</span>

``` c
struct pdo_column_data *columns;
```

<span id="internals2.pdo.stmt.co.cols">\*\*\*\*\*\*</span>

``` c
/* points at the dbh that this statement was prepared on */
    pdo_dbh_t *dbh;

    /* keep track of bound input parameters.  Some drivers support
     * input/output parameters, but you can't rely on that working */
    HashTable *bound_params;
    /* When rewriting from named to positional, this maps positions to names */
    HashTable *bound_param_map; 
    /* keep track of PHP variables bound to named (or positional) columns
     * in the result set */
    HashTable *bound_columns;

    /* not always meaningful */
    long row_count;

    /* used to hold the statement's current query */
    char *query_string;
    int query_stringlen;

    /* the copy of the query with expanded binds ONLY for emulated-prepare drivers */
    char *active_query_string;
    int active_query_stringlen;

    /* the cursor specific error code. */
    pdo_error_type error_code;

    /* used by the query parser for driver specific
     * parameter naming (see pgsql driver for example) */
    const char *named_rewrite_template;
};
```

|                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\*](#internals2.pdo.stmt.co.methods)          | The driver *must* set this during <span class="function">SKEL\_handle\_preparer</span>.                                                                                                                                                                                                                                                                                                                                                                                                            |
| [\*\*](#internals2.pdo.stmt.co.driver-data)    | This item is for use by the driver; the intended usage is to store a pointer (during <span class="function">SKEL\_handle\_factory</span>) to whatever instance data is required to maintain a connection to the database.                                                                                                                                                                                                                                                                          |
| [\*\*\*](#internals2.pdo.stmt.co.executed)     | This is set by PDO after the statement has been executed for the first time. Your driver can inspect this value to determine if it can skip one-time actions as an optimization.                                                                                                                                                                                                                                                                                                                   |
| [\*\*\*\*](#internals2.pdo.stmt.co.holder)     | Discussed in more detail in <a href="/internals2/pdo/implementing.html#internals2.pdo.preparer" class="xref">SKEL_handle_preparer</a>.                                                                                                                                                                                                                                                                                                                                                             |
| [\*\*\*\*\*](#internals2.pdo.stmt.co.colcount) | Your driver is responsible for setting this field to the number of columns available in a result set. This is usually set during <span class="function">SKEL\_stmt\_execute</span> but with some database implementations, the column count may not be available until <span class="function">SKEL\_stmt\_fetch</span> has been called at least once. Drivers that implement <span class="function">SKEL\_stmt\_next\_rowset</span> should update the column count when a new rowset is available. |
| [\*\*\*\*\*\*](#internals2.pdo.stmt.co.cols)   | PDO will allocate this field based on the value that you set for the column count. You are responsible for populating each column during <span class="function">SKEL\_stmt\_describe</span>. You must set the `precision`, `maxlen`, `name`, `namelen` and `param_type` members for each column. The `name` is expected to be allocated using <span class="function">emalloc</span>; PDO will call <span class="function">efree</span> at the appropriate time.                                    |
