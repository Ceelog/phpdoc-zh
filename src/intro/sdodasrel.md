**Warning**

此扩展是*实验性* 的。
此扩展的表象，包括其函数名称以及其他此扩展的相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本扩展风险自担 。

In order to use the Relational Data Access Service for Service Data
Objects, you will need to understand some of the concepts behind SDO:
the data graph, the data object, the disconnected way of working, the
change summary, XPath and property expressions, and so on. If you are
not familiar with these ideas, you might want to look first at
<a href="/ref/sdo.html" class="link">the section on SDO</a>. In
addition, the Relational DAS makes use of the PDO extension to isolate
itself from specifics of different back-end relational databases. In
order to use the Relational DAS you will need to be able to create and
pass a PDO database connection; for this reason you might also want to
take a look at
<a href="/book/pdo.html#简介" class="link">the section on PDO</a>.

The job of the Relational DAS is to move data between the application
and a relational database. In order to do this it needs to be told the
mapping between the database entities - tables, columns, primary keys
and foreign keys - and the elements of the SDO model - types,
properties, containment relationships and so on. You specify this
information as metadata when you construct the Relational DAS.

**Overview of Operation**

1.  The first step is to call the Relational DAS's constructor, passing
    the metadata that defines the mapping between database and SDO
    model. There are examples of this below.

2.  The next step might be to call the <span
    class="function">executeQuery</span> or <span
    class="function">executePreparedQuery</span> methods on the
    Relational DAS, passing either a literal SQL statement for the DAS
    to prepare and execute, or a prepared statement with placeholders
    and a list of values to be inserted. You may also need to specify a
    small amount of metadata about the query itself, so that the
    Relational DAS knows exactly what columns will be returned from the
    database and in what order. You will also need to pass a PDO
    database connection.

    The return value from <span class="function">executeQuery</span> or
    <span class="function">executePreparedQuery</span> is a normalised
    data graph containing all the data from the result set. For a query
    that returns data obtained from a number of tables, this graph will
    contain a number of data objects, linked by SDO containment
    relationships. There may also be SDO non-containment references
    within the data.

    Once the query has been executed and the data graph constructed,
    there is no need for either that instance of the Relational DAS or
    the database connection. There are no locks held on the database.
    Both the Relational DAS and the PDO database connection can be
    garbage collected.

3.  Quite possibly the data in the data graph will go through a number
    of modifications. The data graph can be serialised into the PHP
    session and so may have a lifetime beyond just one client-server
    interaction. Data objects can be created and added to the graph, the
    data objects already in the graph can be deleted, and data objects
    in the graph can be modified.

4.  Finally, the changes made to the data graph can be applied back to
    the database using the <span class="function">applyChanges</span>
    method of the Relational DAS. For this, another instance of the
    Relational DAS must be constructed, using the same metadata, and
    another connection to the database obtained. The connection and the
    data graph are passed to <span class="function">applyChanges</span>.
    At this point the Relational DAS examines the change summary and
    generates the necessary INSERT, UPDATE and DELETE SQL statements to
    apply the changes. Any UPDATE and DELETE statements are qualified
    with the original values of the data so that should the data have
    changed in the database in the meantime this will be detected.
    Assuming no such collisions have occurred the changes will be
    committed to the database. The application can then continue to work
    with the data graph, make more changes and apply them, or can
    discard it.

There are other ways of working with the data in the database: it is
possible to just create data objects and write them to the database
without a preliminary call to <span
class="function">executeQuery</span>, for example. This scenario and
others are explored in the
<a href="/sdodasrel/examples.html" class="link">Examples</a> section
below.
