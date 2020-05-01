pdo\_dbh\_t definition
----------------------

All fields should be treated as read-only by the driver, unless
explicitly stated otherwise.

``` c
/* represents a connection to a database */
struct _pdo_dbh_t {
    /* driver specific methods */
    struct pdo_dbh_methods *methods;
```

<span id="internals2.pdo.dbh.co.methods">\*</span>

``` c
/* driver specific data */
    void *driver_data;
```

<span id="internals2.pdo.dbh.co.driver-data">\*\*</span>

``` c
/* credentials */
    char *username, *password;
```

<span id="internals2.pdo.dbh.co.credentials">\*\*\*</span>

``` c
/* if true, then data stored and pointed at by this handle must all be
     * persistently allocated */
    unsigned is_persistent:1;
```

<span id="internals2.pdo.dbh.co.is-persist">\*\*\*\*</span>

``` c
/* if true, driver should act as though a COMMIT were executed between
     * each executed statement; otherwise, COMMIT must be carried out manually
     * */
    unsigned auto_commit:1;
```

<span id="internals2.pdo.dbh.co.auto-commit">\*\*\*\*\*</span>

``` c
/* if true, the driver requires that memory be allocated explicitly for
     * the columns that are returned */
    unsigned alloc_own_columns:1;
```

<span id="internals2.pdo.dbh.co.alloc-own">\*\*\*\*\*\*</span>

``` c
/* if true, commit or rollBack is allowed to be called */
    unsigned in_txn:1;                  

    /* max length a single character can become after correct quoting */
    unsigned max_escaped_char_length:3;
```

<span id="internals2.pdo.dbh.co.max-esc">\*\*\*\*\*\*\*</span>

``` c
/* data source string used to open this handle */
    const char *data_source;
```

<span id="internals2.pdo.dbh.co.dsn">\*\*\*\*\*\*\*\*</span>

``` c
unsigned long data_source_len;

    /* the global error code. */
    pdo_error_type error_code;
```

<span id="internals2.pdo.dbh.co.error-code">\*\*\*\*\*\*\*\*\*</span>

``` c
enum pdo_case_conversion native_case
```

<span id="internals2.pdo.dbh.co-ncase">\*\*\*\*\*\*\*\*\*\*</span>

``` c
, desired_case;
};
```

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="#internals2.pdo.dbh.co.methods">*</a></td>
<td><p>The driver <em>must</em> set this during <span class="function">SKEL_handle_factory</span>.</p></td>
</tr>
<tr class="even">
<td><a href="#internals2.pdo.dbh.co.driver-data">**</a></td>
<td><p>This item is for use by the driver; the intended usage is to store a pointer (during <span class="function">SKEL_handle_factory</span>) to whatever instance data is required to maintain a connection to the database.</p></td>
</tr>
<tr class="odd">
<td><a href="#internals2.pdo.dbh.co.credentials">***</a></td>
<td><p>The username and password that were passed into the PDO constructor. The driver should use these values when it initiates a connection to the database.</p></td>
</tr>
<tr class="even">
<td><a href="#internals2.pdo.dbh.co.is-persist">****</a></td>
<td><p>If this is set to 1, then any data that is referenced by the dbh, including whatever structure your driver allocates, <em>MUST</em> be allocated persistently. This is easy to achieve; rather than using the usual <span class="function">emalloc</span> simply use <span class="function">pemalloc</span> and pass the value of this flag as the last parameter. Failure to use the appropriate kind of memory can lead to serious memory faults, resulting (in the best case) a hard crash, and in the worst case, an exploitable memory problem.</p>
<p>If, for whatever reason, your driver is not suitable to run persistently, you <em>MUST</em> check this flag in your <span class="function">SKEL_handle_factory</span> and raise an appropriate error.</p></td>
</tr>
<tr class="odd">
<td><a href="#internals2.pdo.dbh.co.auto-commit">*****</a></td>
<td><p>You should check this value in your <span class="function">SKEL_handle_doer</span> and <span class="function">SKEL_stmt_execute</span> functions; if it evaluates to true, you must attempt to commit the query now. Most database implementations offer an auto-commit mode that handles this automatically.</p></td>
</tr>
<tr class="even">
<td><a href="#internals2.pdo.dbh.co.alloc-own">******</a></td>
<td><p>If your database client library API operates by fetching data into a caller-supplied buffer, you should set this flag to 1 during your <span class="function">SKEL_handle_factory</span>. When set, PDO will call your <span class="function">SKEL_stmt_describer</span> earlier than it would otherwise. This early call allows you to determine those buffer sizes and issue appropriate calls to the database client library.</p>
<p>If your database client library API simply returns pointers to its own internal buffers for you to copy after each fetch call, you should leave this value set to 0.</p></td>
</tr>
<tr class="odd">
<td><a href="#internals2.pdo.dbh.co.max-esc">*******</a></td>
<td><p>If your driver doesn't support native prepared statements (<code class="parameter">supports_placeholders</code> is set to <strong><code>PDO_PLACEHOLDER_NONE</code></strong>), you must set this value to the maximum length that can be taken up by a single character when it is quoted by your <span class="function">SKEL_handle_quoter</span> function. This value is used to calculate the amount of buffer space required when PDO executes the statement.</p></td>
</tr>
<tr class="even">
<td><a href="#internals2.pdo.dbh.co.dsn">********</a></td>
<td><p>This holds the value of the DSN that was passed into the PDO constructor. If your driver implementation needed to modify the DSN for whatever reason, it should update this member during <span class="function">SKEL_handle_factory</span>. Modifying this member should be avoided. If you do change it, you must ensure that <code class="parameter">data_source_len</code> is also correct.</p></td>
</tr>
<tr class="odd">
<td><a href="#internals2.pdo.dbh.co.error-code">*********</a></td>
<td><p>Whenever an error occurs during a call to one of your driver methods, you should set this member to the SQLSTATE code that best describes the error and return an error. In this HOW-TO, the suggested practice is to call <span class="function">SKEL_handle_error</span> when an error is detected, and have it set the error code.</p></td>
</tr>
<tr class="even">
<td><a href="#internals2.pdo.dbh.co-ncase">**********</a></td>
<td><p>Your driver should set this during <span class="function">SKEL_handle_factory</span>; the value should reflect how the database returns the names of the columns in result sets. If the name matches the case that was used in the query, set it to <strong><code>PDO_CASE_NATURAL</code></strong> (this is actually the default). If the column names are always returned in upper case, set it to <strong><code>PDO_CASE_UPPER</code></strong>. If the column names are always returned in lower case, set it to <strong><code>PDO_CASE_LOWER</code></strong>. The value you set is used to determine if PDO should perform case folding when the user sets the <strong><code>PDO_ATTR_CASE</code></strong> attribute.</p></td>
</tr>
</tbody>
</table>
