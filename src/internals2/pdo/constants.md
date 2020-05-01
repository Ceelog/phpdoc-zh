Constants
---------

<table>
<caption><strong>Database and Statement Attributes Table</strong></caption>
<tbody>
<tr class="odd">
<td><p>Attribute</p></td>
<td><p>Valid value(s)</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_AUTOCOMMIT</p></td>
<td><p>BOOL</p>
<p>TRUE if autocommit is set, FALSE otherwise.</p>
<p>dbh-&gt;auto_commit contains value. Processed by PDO directly.</p></td>
</tr>
<tr class="odd">
<td><p>PDO_ATTR_PREFETCH</p></td>
<td><p>LONG</p>
<p>Value of the prefetch size in drivers that support it.</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_TIMEOUT</p></td>
<td><p>LONG</p>
<p>How long to wait for a db operation before timing out.</p></td>
</tr>
<tr class="odd">
<td><p>PDO_ATTR_ERRMODE</p></td>
<td><p>LONG</p>
<p>Processed and handled by PDO</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_SERVER_VERSION</p></td>
<td><p>STRING</p>
<p>The “human-readable” string representing the Server/Version this driver is currently connected to.</p></td>
</tr>
<tr class="odd">
<td><p>PDO_ATTR_CLIENT_VERSION</p></td>
<td><p>STRING</p>
<p>The “human-readable” string representing the Client/Version this driver supports.</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_SERVER_INFO</p></td>
<td><p>STRING</p>
<p>The “human-readable” description of the Server.</p></td>
</tr>
<tr class="odd">
<td><p>PDO_ATTR_CONNECTION_STATUS</p></td>
<td><p>LONG</p>
<p>Values not yet defined</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_CASE</p></td>
<td><p>LONG</p>
<p>Processed and handled by PDO.</p></td>
</tr>
<tr class="odd">
<td><p>PDO_ATTR_CURSOR_NAME</p></td>
<td><p>STRING</p>
<p>String representing the name for a database cursor for use in “where current in &lt;name&gt;” SQL statements.</p></td>
</tr>
<tr class="even">
<td><p>PDO_ATTR_CURSOR</p></td>
<td><p>LONG</p>
<dl>
<dt>PDO_CURSOR_FWDONLY</dt>
<dd><p>Forward only cursor</p>
</dd>
<dt>PDO_CURSOR_SCROLL</dt>
<dd><p>Scrollable cursor</p>
</dd>
</dl></td>
</tr>
</tbody>
</table>

The values for the attributes above are all defined in terms of the Zend
API. The Zend API contains macros that can be used to convert a \*zval
to a value. These macros are defined in the Zend header file,
zend\_API.h in the Zend directory of your PHP build directory. Some of
these attributes can be used with the statement attribute handlers such
as the PDO\_ATTR\_CURSOR and PDO\_ATTR\_CURSOR\_NAME. See the statement
attribute handling functions for more information.
