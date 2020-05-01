Service Data Objects (SDOs) enable PHP applications to work with data
from different sources (like a database query, an XML file, and a
spreadsheet) using a single interface.

Each different kind of data source requires a Data Access Service (DAS)
to provide access to the data in the data source. In your PHP
application, you use a DAS to create an SDO instance that represents
some data in the data source. You can then set and get values in the SDO
instance using the standard SDO interface. Finally, you use a DAS to
write the modified data back to a data source, typically the same one.

See the
<a href="/ref/sdo.html#Data%20Access%20Services" class="link">list of Data Access Services</a>
for details on those currently available. In addition to the provided
DASs, SDO also provides interfaces to enable others to be implemented
(see the section on
<a href="/ref/sdo.html#SDO%20Data%20Access%20Service%20Developer%20Interfaces" class="link">SDO Data Access Services Interface</a>
for more details).

This extension is derived from concepts taken from the
<a href="https://www.jcp.org/en/jsr/detail?id=235" class="link external">» Service Data Objects specification</a>.
It includes a version of the
<a href="http://tuscany.apache.org/" class="link external">» Apache Tuscany</a>
SDO for C++ project.

The Structure of a Service Data Object
--------------------------------------

A Service Data Object instance is made up of a tree of data objects. The
tree is defined by containment relationships between the data objects.
For example, a Company data object might consist of a number of
Department data objects and therefore the Company would have a
containment relationship to the Departments.

An SDO may also have non-containment references between data objects in
the tree. For example, one Employee data object might reference another
Employee to identify a career mentor.

As well as data objects referencing each other, they can also have
primitive properties. For example, the Company data object might have a
property called "name" of type string, for holding the name of the
company (for example, "Acme").

Each of these properties of a data object - containment relationships,
non-containment references, or primitive properties - may be many-valued
or single-valued. In the above examples, Departments is many-valued and
the Company name is single-valued.

In PHP, each SDO data object is represented as a PHP object. The
properties of the data object can be accessed using either object syntax
or associative array syntax. We'll see some examples of this later.
