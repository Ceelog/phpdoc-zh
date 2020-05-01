Fleshing out your skeleton
--------------------------

### Major Structures and Attributes

The major structures, pdo\_dbh\_t and pdo\_stmt\_t are defined and
explained in Appendix A and B respectively. Database and Statement
attributes are defined in Appendix C. Error handling is explained in
Appendix D.

### pdo\_SKEL.c: PHP extension glue

#### function entries

``` synopsis
static function_entry pdo_SKEL_functions[] = {
  { NULL, NULL, NULL }
};
```

This structure is used to register functions into the global php
function namespace. PDO drivers should try to avoid doing this, so it is
recommended that you leave this structure initialized to NULL, as shown
in the synopsis above.

#### Module entry

``` synopsis
/* {{{ pdo_SKEL_module_entry */
#if ZEND_EXTENSION_API_NO >= 220050617
static zend_module_dep pdo_SKEL_deps[] = {
    ZEND_MOD_REQUIRED("pdo")
    {NULL, NULL, NULL}
};
#endif
/* }}} */

zend_module_entry pdo_SKEL_module_entry = {
#if ZEND_EXTENSION_API_NO >= 220050617
    STANDARD_MODULE_HEADER_EX, NULL,
    pdo_SKEL_deps,
#else
    STANDARD_MODULE_HEADER,
#endif
    "pdo_SKEL",
    pdo_SKEL_functions,
    PHP_MINIT(pdo_SKEL),
    PHP_MSHUTDOWN(pdo_SKEL),
    NULL,
    NULL,
    PHP_MINFO(pdo_SKEL),
    PHP_PDO_<DB>_MODULE_VERSION,
    STANDARD_MODULE_PROPERTIES
};
/* }}} */

#ifdef COMPILE_DL_PDO_<DB>
ZEND_GET_MODULE(pdo_db)
#endif
```

A structure of type zend\_module\_entry called pdo\_SKEL\_module\_entry
must be declared and should include reference to the
pdo\_SKEL\_functions table defined previously.

#### Standard PHP Module Extension Functions

##### PHP\_MINIT\_FUNCTION

``` synopsis
/* {{{ PHP_MINIT_FUNCTION */
PHP_MINIT_FUNCTION(pdo_SKEL)
{
    return php_pdo_register_driver(&pdo_SKEL_driver);
}
/* }}} */
```

This standard PHP extension function should be used to register your
driver with the PDO layer. This is done by calling the <span
class="function">php\_pdo\_register\_driver</span> function passing a
pointer to a structure of type <span class="type">pdo\_driver\_t</span>
typically named *pdo\_SKEL\_driver*. A <span
class="type">pdo\_driver\_t</span> contains a header that is generated
using the *PDO\_DRIVER\_HEADER(SKEL)* macro and <span
class="function">pdo\_SKEL\_handle\_factory</span> function pointer. The
actual function is described during the discussion of the `SKEL_dbh.c`
unit.

##### PHP\_MSHUTDOWN\_FUNCTION

``` synopsis
/* {{{ PHP_MSHUTDOWN_FUNCTION */
PHP_MSHUTDOWN_FUNCTION(pdo_SKEL)
{
    php_pdo_unregister_driver(&pdo_SKEL_driver);
    return SUCCESS;
}
/* }}} */
```

This standard PHP extension function is used to unregister your driver
from the PDO layer. This is done by calling the <span
class="function">php\_pdo\_unregister\_driver</span> function, passing
the same *pdo\_SKEL\_driver* structure that was passed in the init
function above.

##### PHP\_MINFO\_FUNCTION

This is again a standard PHP extension function. Its purpose is to
display information regarding the module when the <span
class="function">phpinfo</span> is called from a script. The convention
is to display the version of the module and also what version of the db
you are dependent on, along with any other configuration style
information that might be relevant.

### SKEL\_driver.c: Driver implementation

This unit implements all of the database handling methods that support
the PDO database handle object. It also contains the error fetching
routines. All of these functions will typically need to access the
global variable pool. Therefore, it is necessary to use the Zend macro
TSRMLS\_DC macro at the end of each of these statements. Consult the
Zend programmer documentation for more information on this macro.

#### pdo\_SKEL\_error

``` synopsis
static int pdo_SKEL_error(pdo_dbh_t *dbh,
  pdo_stmt_t *stmt, const char *file, int line TSRMLS_DC)
```

The purpose of this function is to be used as a generic error handling
function within the driver. It is called by the driver when an error
occurs within the driver. If an error occurs that is not related to
SQLSTATE, the driver should set either *dbh-\>error\_code* or
*stmt-\>error\_code* to an SQLSTATE that most closely matches the error
or the generic SQLSTATE error “HY000”. The file pdo\_sqlstate.c in the
PDO source contains a table of commonly used SQLSTATE codes that the PDO
code explicitly recognizes. This setting of the error code should be
done prior to calling this function.; This function should set the
global `pdo_err` variable to the error found in either the dbh or the
stmt (if the variable stmt is not NULL).

dbh  
Pointer to the database handle initialized by the handle factory

stmt  
Pointer to the current statement or NULL. If NULL, the error is derived
by error code found in the dbh.

file  
The source file where the error occurred or NULL if not available.

line  
The line number within the source file if available.

If the dbh member methods is NULL (which implies that the error is being
raised from within the PDO constructor), this function should call the
zend\_throw\_exception\_ex() function otherwise it should return the
error code. This function is usually called using a helper macro that
customizes the calling sequence for either database handling errors or
statement handling errors.

**示例 \#1 Example macros for invoking pdo\_SKEL\_error**

``` c
#define pdo_SKEL_drv_error(what) \
    pdo_SKEL_error(dbh, NULL, what, __FILE__, __LINE__ TSRMLS_CC)
#define pdo_SKEL_drv_error(what) \
    pdo_SKEL_error(dbh, NULL, what, __FILE__, __LINE__ TSRMLS_CC)
```

For more info on error handling, see
<a href="/internals2/pdo/error-handling.html" class="xref">Error handling</a>.

> **Note**:
>
> Despite being documented here, the PDO driver interface does not
> specify that this function be present; it is merely a convenient way
> to handle errors, and it just happens to be equally convenient for the
> majority of database client library APIs to structure your driver
> implementation in this way.

#### pdo\_SKEL\_fetch\_error\_func

``` synopsis
static int pdo_SKEL_fetch_error_func(pdo_dbh_t *dbh, pdo_stmt_t *stmt,
    zval *info TSRMLS_DC)
```

The purpose of this function is to obtain additional information about
the last error that was triggered. This includes the driver specific
error code and a human readable string. It may also include additional
information if appropriate. This function is called as a result of the
PHP script calling the <span class="function">PDO::errorInfo</span>
method.

dbh  
Pointer to the database handle initialized by the handle factory

stmt  
Pointer to the most current statement or NULL. If NULL, the error
translated is derived by error code found in the dbh.

info  
A hash table containing error codes and messages.

The error\_func should return two pieces of information as successive
array elements. The first item is expected to be a numeric error code,
the second item is a descriptive string. The best way to set this item
is by using add\_next\_index. Note that the type of the first argument
need not be <span class="type">long</span>; use whichever type most
closely matches the error code returned by the underlying database API.

``` c
/* now add the error information. */
/* These need to be added in a specific order */
add_next_index_long(info, error_code);   /* driver specific error code */
add_next_index_string(info, message, 0); /* readable error message */
```

This function should return 1 if information is available, 0 if the
driver does not have additional info.

#### SKEL\_handle\_closer

``` synopsis
static int SKEL_handle_closer(pdo_dbh_t *dbh TSRMLS_DC)
```

This function will be called by PDO to close an open database.

dbh  
Pointer to the database handle initialized by the handle factory

This should do whatever database specific activity that needs to be
accomplished to close the open database. PDO ignores the return value
from this function.

#### SKEL\_handle\_preparer

``` synopsis
static int SKEL_handle_preparer(pdo_dbh_t *dbh, const char *sql,
long sql_len, pdo_stmt_t *stmt, zval *driver_options TSRMLS_DC)
```

This function will be called by PDO in response to <span
class="function">PDO::query</span> and <span
class="function">PDO::prepare</span> calls from the PHP script. The
purpose of the function is to prepare raw SQL for execution, storing
whatever state is appropriate into the `stmt` that is passed in.

dbh  
Pointer to the database handle initialized by the handle factory

sql  
Pointer to a character string containing the SQL statement to be
prepared.

sql\_len  
The length of the SQL statement.

Stmt  
Pointer to the returned statement or NULL if an error occurs.

driver\_options  
Any driver specific/defined options.

This function is essentially the constructor for a stmt object. This
function is responsible for processing statement options, and setting
driver-specific option fields in the pdo\_stmt\_t structure.

PDO does not process any statement options on the driver's behalf before
calling the preparer function. It is your responsibility to process them
before you return, raising an error for any unknown options that are
passed.

One very important responsibility of this function is the processing of
SQL statement parameters. At the time of this call, PDO does not know if
your driver supports binding parameters into prepared statements, nor
does it know if it supports named or positional parameter naming
conventions.

Your driver is responsible for setting *stmt-\>supports\_placeholders*
as appropriate for the underlying database. This may involve some
run-time determination on the part of your driver, if this setting
depends on the version of the database server to which it is connected.
If your driver doesn't directly support both named and positional
parameter conventions, you should use the <span
class="function">pdo\_parse\_params</span> API to have PDO rewrite the
query to take advantage of the support provided by your database.

**示例 \#2 Using pdo\_parse\_params**

``` c
int ret;
    char *nsql = NULL;
    int nsql_len = 0;

    /* before we prepare, we need to peek at the query; if it uses named parameters,
     * we want PDO to rewrite them for us */
    stmt->supports_placeholders = PDO_PLACEHOLDER_POSITIONAL;
    ret = pdo_parse_params(stmt, (char*)sql, sql_len, &nsql, &nsql_len TSRMLS_CC);

    if (ret == 1) {
        /* query was re-written */
        sql = nsql;
    } else if (ret == -1) {
        /* couldn't grok it */
        strcpy(dbh->error_code, stmt->error_code);
        return 0;
    }

    /* now proceed to prepare the query in "sql" */
```

Possible values for *supports\_placeholders* are:
**`PDO_PLACEHOLDER_NAMED`**, **`PDO_PLACEHOLDER_POSITIONAL`** and
**`PDO_PLACEHOLDER_NONE`**. If the driver doesn't support prepare
statements at all, then this function should simply allocate any state
that it might need, and then return:

**示例 \#3 Implementing preparer for drivers that don't support native
prepared statements**

``` c
static int SKEL_handle_preparer(pdo_dbh_t *dbh, const char *sql,
    long sql_len, pdo_stmt_t *stmt, zval *driver_options TSRMLS_DC)
{
    pdo_SKEL_db_handle *H = (pdo_SKEL_db_handle *)dbh->driver_data;
    pdo_SKEL_stmt *S = ecalloc(1, sizeof(pdo_SKEL_stmt));

    S->H = H;
    stmt->driver_data = S;
    stmt->methods = &SKEL_stmt_methods;
    stmt->supports_placeholders = PDO_PLACEHOLDER_NONE;

    return 1;
}
```

This function returns 1 on success or 0 on failure.

#### SKEL\_handle\_doer

``` synopsis
static long SKEL_handle_doer(pdo_dbh_t *dbh, const char *sql, long sql_len TSRMLS_DC)
```

This function will be called by PDO to execute a raw SQL statement. No
pdo\_stmt\_t is created.

dbh  
Pointer to the database handle initialized by the handle factory

sql  
Pointer to a character string containing the SQL statement to be
prepared.

sql\_len  
The length of the SQL statement.

This function returns 1 on success or 0 on failure.

#### SKEL\_handle\_quoter

``` synopsis
static int SKEL_handle_quoter(pdo_dbh_t *dbh, const char *unquoted,
  int unquoted_len, char **quoted, int quoted_len, enum pdo_param_type param_type TSRMLS_DC)
```

This function will be called by PDO to turn an unquoted string into a
quoted string for use in a query.

dbh  
Pointer to the database handle initialized by the handle factory

unquoted  
Pointer to a character string containing the string to be quoted.

unquoted\_len  
The length of the string to be quoted.

quoted  
Pointer to the address where a pointer to the newly quoted string will
be returned.

quoted\_len  
The length of the new string.

param\_type  
A driver specific hint for driver that have alternate quoting styles

This function is called in response to a call to <span
class="function">PDO::quote</span> or when the driver has set
*supports\_placeholder* to **`PDO_PLACEHOLDER_NONE`**. The purpose is to
quote a parameter when building SQL statements.

If your driver does not support native prepared statements,
implementation of this function is required.

This function returns 1 if the quoting process reformatted the string,
and 0 if it was not necessary to change the string. The original string
will be used unchanged with a 0 return.

#### SKEL\_handle\_begin

``` synopsis
static int SKEL_handle_begin(pdo_dbh_t *dbh TSRMLS_DC)
```

This function will be called by PDO to begin a database transaction.

dbh  
Pointer to the database handle initialized by the handle factory

This should do whatever database specific activity that needs to be
accomplished to begin a transaction. This function returns 1 for success
or 0 if an error occurred.

#### SKEL\_handle\_commit

``` synopsis
static int SKEL_handle_commit(pdo_dbh_t *dbh TSRMLS_DC)
```

This function will be called by PDO to end a database transaction.

dbh  
Pointer to the database handle initialized by the handle factory

This should do whatever database specific activity that needs to be
accomplished to commit a transaction. This function returns 1 for
success or 0 if an error occurred.

#### SKEL\_handle\_rollback

``` synopsis
static int SKEL_handle_rollback( pdo_dbh_t *dbh TSRMLS_DC)
```

This function will be called by PDO to rollback a database transaction.

dbh  
Pointer to the database handle initialized by the handle factory

This should do whatever database specific activity that needs to be
accomplished to rollback a transaction. This function returns 1 for
success or 0 if an error occurred.

#### SKEL\_handle\_get\_attribute

``` synopsis
static int SKEL_handle_get_attribute(pdo_dbh_t *dbh, long attr, zval *return_value TSRMLS_DC)
```

This function will be called by PDO to retrieve a database attribute.

dbh  
Pointer to the database handle initialized by the handle factory

attr  
<span class="type">long</span> value of one of the PDO\_ATTR\_xxxx
types. See
<a href="/internals2/pdo/constants.html#internals2.pdo.table.attributes" class="xref">Database and Statement Attributes Table</a>
for valid attributes.

return\_value  
The returned value for the attribute.

It is up to the driver to decide which attributes will be supported for
a particular implementation. It is not necessary for a driver to supply
this function. PDO driver handles the PDO\_ATTR\_PERSISTENT,
PDO\_ATTR\_CASE, PDO\_ATTR\_ORACLE\_NULLS, and PDO\_ATTR\_ERRMODE
attributes directly.

This function returns 1 on success or 0 on failure.

#### SKEL\_handle\_set\_attribute

``` synopsis
static int SKEL_handle_set_attribute(pdo_dbh_t *dbh, long attr, zval *val TSRMLS_DC)
```

This function will be called by PDO to set a database attribute, usually
in response to a script calling <span
class="function">PDO::setAttribute</span>.

dbh  
Pointer to the database handle initialized by the handle factory

attr  
<span class="type">long</span> value of one of the PDO\_ATTR\_xxxx
types. See
<a href="/internals2/pdo/constants.html#internals2.pdo.table.attributes" class="xref">Database and Statement Attributes Table</a>
for valid attributes.

val  
The new value for the attribute.

It is up to the driver to decide which attributes will be supported for
a particular implementation. It is not necessary for a driver to provide
this function if it does not need to support additional attributes. The
PDO driver handles the PDO\_ATTR\_CASE, PDO\_ATTR\_ORACLE\_NULLS, and
PDO\_ATTR\_ERRMODE attributes directly.

This function returns 1 on success or 0 on failure.

#### SKEL\_handle\_last\_id

``` synopsis
static char * SKEL_handle_last_id(pdo_dbh_t *dbh, const char *name, unsigned int len TSRMLS_DC)
```

This function will be called by PDO to retrieve the ID of the last
inserted row.

dbh  
Pointer to the database handle initialized by the handle factory

name  
string representing a table or sequence name.

len  
the length of the `name` parameter.

This function returns a character string containing the id of the last
inserted row on success or NULL on failure. This is an optional
function.

#### SKEL\_check\_liveness

``` synopsis
static int SKEL_check_liveness(pdo_dbh_t *dbh TSRMLS_DC)
```

This function will be called by PDO to test whether or not a persistent
connection to a database is alive and ready for use.

dbh  
Pointer to the database handle initialized by the handle factory

This function returns 1 if the database connection is alive and ready
for use, otherwise it should return 0 to indicate failure or lack of
support.

> **Note**:
>
> This is an optional function.

#### SKEL\_get\_driver\_methods

``` synopsis
static function_entry *SKEL_get_driver_methods(pdo_dbh_t *dbh, int kind TSRMLS_DC)
```

This function will be called by PDO in response to a call to any method
that is not a part of either the <span class="classname">PDO</span> or
<span class="classname">PDOStatement</span> classes. It's purpose is to
allow the driver to provide additional driver specific methods to those
classes.

dbh  
Pointer to the database handle initialized by the handle factory

kind  
One of the following:

PDO\_DBH\_DRIVER\_METHOD\_KIND\_DBH  
Set when the method call was attempted on an instance of the <span
class="classname">PDO</span> class. The driver should return a pointer a
function\_entry table for any methods it wants to add to that class, or
NULL if there are none.

PDO\_DBH\_DRIVER\_METHOD\_KIND\_STMT  
Set when the method call was attempted on an instance of the <span
class="classname">PDOStatement</span> class. The driver should return a
pointer to a function\_entry table for any methods it wants to add to
that class, or NULL if there are none.

This function returns a pointer to the function\_entry table requested,
or NULL there are no driver specific methods.

#### SKEL\_handle\_factory

``` synopsis
static int SKEL_handle_factory(pdo_dbh_t *dbh, zval *driver_options TSRMLS_DC)
```

This function will be called by PDO to create a database handle. For
most databases this involves establishing a connection to the database.
In some cases, a persistent connection may be requested, in other cases
connection pooling may be requested. All of these are database/driver
dependent.

dbh  
Pointer to the database handle initialized by the handle factory

driver\_options  
An array of driver options, keyed by integer option number. See
<a href="/internals2/pdo/constants.html#internals2.pdo.table.attributes" class="xref">Database and Statement Attributes Table</a>
for a list of possible attributes.

This function should fill in the passed database handle structure with
its driver specific information on success and return 1, otherwise it
should return 0 to indicate failure.

PDO processes the AUTOCOMMIT and PERSISTENT driver options before
calling the handle\_factory. It is the handle factory's responsibility
to process other options.

#### Driver method table

A static structure of type pdo\_dbh\_methods named SKEL\_methods must be
declared and initialized to the function pointers for each defined
function. If a function is not supported or not implemented the value
for that function pointer should be set to NULL.

#### pdo\_SKEL\_driver

A structure of type pdo\_driver\_t named pdo\_SKEL\_driver should be
declared. The PDO\_DRIVER\_HEADER(SKEL) macro should be used to declare
the header and the function pointer to the handle factory function
should set.

### SKEL\_statement.c: Statement implementation

This unit implements all of the database statement handling methods that
support the PDO statement object.

#### SKEL\_stmt\_dtor

``` synopsis
static int SKEL_stmt_dtor(pdo_stmt_t *stmt TSRMLS_DC)
```

This function will be called by PDO to destroy a previously constructed
statement object.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

This should do whatever is necessary to free up any driver specific
storage allocated for the statement. The return value from this function
is ignored.

#### SKEL\_stmt\_execute

``` synopsis
static int SKEL_stmt_execute(pdo_stmt_t *stmt TSRMLS_DC)
```

This function will be called by PDO to execute the prepared SQL
statement in the passed statement object.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

This function returns 1 for success or 0 in the event of failure.

#### SKEL\_stmt\_fetch

``` synopsis
static int SKEL_stmt_fetch(pdo_stmt_t *stmt, enum pdo_fetch_orientation ori,
   long offset TSRMLS_DC)
```

This function will be called by PDO to fetch a row from a previously
executed statement object.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

ori  
One of PDO\_FETCH\_ORI\_xxx which will determine which row will be
fetched.

offset  
If ori is set to PDO\_FETCH\_ORI\_ABS or PDO\_FETCH\_ORI\_REL, offset
represents the row desired or the row relative to the current position,
respectively. Otherwise, this value is ignored.

The results of this fetch are driver dependent and the data is usually
stored in the driver\_data member of the pdo\_stmt\_t object. The ori
and offset parameters are only meaningful if the statement represents a
scrollable cursor. This function returns 1 for success or 0 in the event
of failure.

#### SKEL\_stmt\_param\_hook

``` synopsis
static int SKEL_stmt_param_hook(pdo_stmt_t *stmt,
  struct pdo_bound_param_data *param, enum pdo_param_event event_type TSRMLS_DC)
```

This function will be called by PDO for handling of both bound
parameters and bound columns.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

param  
The structure describing either a statement parameter or a bound column.

event\_type  
The type of event to occur for this parameter, one of the following:

PDO\_PARAM\_EVT\_ALLOC  
Called when PDO allocates the binding. Occurs as part of <span
class="function">PDOStatement::bindParam</span>, <span
class="function">PDOStatement::bindValue</span> or as part of an
implicit bind when calling <span
class="function">PDOStatement::execute</span>. This is your opportunity
to take some action at this point; drivers that implement native
prepared statements will typically want to query the parameter
information, reconcile the type with that requested by the script,
allocate an appropriately sized buffer and then bind the parameter to
that buffer. You should not rely on the type or value of the zval at
*param-\>parameter* at this point in time.

PDO\_PARAM\_EVT\_FREE  
Called once per parameter as part of cleanup. You should release any
resources associated with that parameter now.

PDO\_PARAM\_EXEC\_PRE  
Called once for each parameter immediately before calling
SKEL\_stmt\_execute; take this opportunity to make any final adjustments
ready for execution. In particular, you should note that variables bound
via <span class="function">PDOStatement::bindParam</span> are only legal
to touch now, and not any sooner.

PDO\_PARAM\_EXEC\_POST  
Called once for each parameter immediately after calling
SKEL\_stmt\_execute; take this opportunity to make any post-execution
actions that might be required by your driver.

PDO\_PARAM\_FETCH\_PRE  
Called once for each parameter immediately prior to calling
SKEL\_stmt\_fetch.

PDO\_PARAM\_FETCH\_POST  
Called once for each parameter immediately after calling
SKEL\_stmt\_fetch.

This hook will be called for each bound parameter and bound column in
the statement. For ALLOC and FREE events, a single call will be made for
each parameter or column. The param structure contains a driver\_data
field that the driver can use to store implementation specific
information about each of the parameters.

For all other events, PDO may call you multiple times as the script
issues <span class="function">PDOStatement::execute</span> and <span
class="function">PDOStatement::fetch</span> calls.

If this is a bound parameter, the is\_param flag in the param structure
is set, otherwise the param structure refers to a bound column.

This function returns 1 for success or 0 in the event of failure.

#### SKEL\_stmt\_describe\_col

``` synopsis
static int SKEL_stmt_describe_col(pdo_stmt_t *stmt, int colno TSRMLS_DC)
```

This function will be called by PDO to query information about a
particular column.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

colno  
The column number to be queried.

The driver should populate the pdo\_stmt\_t member columns(colno) with
the appropriate information. This function returns 1 for success or 0 in
the event of failure.

#### SKEL\_stmt\_get\_col\_data

``` synopsis
static int SKEL_stmt_get_col_data(pdo_stmt_t *stmt, int colno,
  char **ptr, unsigned long *len, int *caller_frees TSRMLS_DC)
```

This function will be called by PDO to retrieve data from the specified
column.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

colno  
The column number to be queried.

ptr  
Pointer to the retrieved data.

len  
The length of the data pointed to by ptr.

caller\_frees  
If set, ptr should point to emalloc'd memory and the main PDO driver
will free it as soon as it is done with it. Otherwise, it will be the
responsibility of the driver to free any allocated memory as a result of
this call.

The driver should return the resultant data and length of that data in
the ptr and len variables respectively. It should be noted that the main
PDO driver expects the driver to manage the lifetime of the data. This
function returns 1 for success or 0 in the event of failure.

#### SKEL\_stmt\_set\_attr

``` synopsis
static int SKEL_stmt_set_attr(pdo_stmt_t *stmt, long attr, zval *val TSRMLS_DC)
```

This function will be called by PDO to allow the setting of driver
specific attributes for a statement object.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

attr  
<span class="type">long</span> value of one of the PDO\_ATTR\_xxxx
types. See
<a href="/internals2/pdo/constants.html#internals2.pdo.table.attributes" class="xref">Database and Statement Attributes Table</a>
for valid attributes.

val  
The new value for the attribute.

This function is driver dependent and allows the driver the capability
to set database specific attributes for a statement. This function
returns 1 for success or 0 in the event of failure. This is an optional
function. If the driver does not support additional settable attributes,
it can be NULLed in the method table. The PDO driver does not handle any
settable attributes on the database driver's behalf.

#### SKEL\_stmt\_get\_attr

``` synopsis
static int SKEL_stmt_get_attr(pdo_stmt_t *stmt, long attr, zval
   *return_value TSRMLS_DC)
```

This function will be called by PDO to allow the retrieval of driver
specific attributes for a statement object.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

attr  
<span class="type">long</span> value of one of the PDO\_ATTR\_xxxx
types. See
<a href="/internals2/pdo/constants.html#internals2.pdo.table.attributes" class="xref">Database and Statement Attributes Table</a>
for valid attributes.

return\_value  
The returned value for the attribute.

This function is driver dependent and allows the driver the capability
to retrieve a previously set database specific attribute for a
statement. This function returns 1 for success or 0 in the event of
failure. This is an optional function. If the driver does not support
additional gettable attributes, it can be NULLed in the method table.
The PDO driver does not handle any settable attributes on the database
driver's behalf.

#### SKEL\_stmt\_get\_col\_meta

``` synopsis
static int SKEL_stmt_get_col_meta(pdo_stmt_t *stmt, int colno,
   zval *return_value TSRMLS_DC)
```

**Warning**

This function is not well defined and is subject to change.

This function will be called by PDO to retrieve meta data from the
specified column.

stmt  
Pointer to the statement structure initialized by
SKEL\_handle\_preparer.

colno  
The column number for which data is to be retrieved.

return\_value  
Holds the returned meta data.

The driver author should consult the documentation for this function
that can be found in the php\_pdo\_driver.h header as this will be the
most current. This function returns **`SUCCESS`** for success or
**`FAILURE`** in the event of failure. The database driver does not need
to provide this function.

#### Statement handling method table

A static structure of type pdo\_stmt\_methods named SKEL\_stmt\_methods
should be declared and initialized to the function pointers for each
defined function. If a function is not supported or not implemented the
value for that function pointer should be set to NULL.
