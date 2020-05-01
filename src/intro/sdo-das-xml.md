In order to use the XML Data Access Service for Service Data Objects,
you will need to understand some of the concepts behind SDO: the data
graph, the data object, XPath and property expressions, and so on. If
you are not familiar with these ideas, you might want to look first at
<a href="/ref/sdo.html" class="link">the section on SDO</a>.

The job of the XML DAS is to move data between the application and an
XML data source, which can be either a file or a URL. SDOs are always
created and maintained according to a model which defines type names and
what property names each type may have. For data which is from XML, this
SDO model is built from a schema file written in XML schema language (an
xsd file). This schema file is usually passed to the create method when
the XMLDAS is initialised. The
<a href="https://www.jcp.org/en/jsr/detail?id=235" class="link external">» SDO 2.0 specification</a>
defines the mapping between XML types and SDO types. There are a number
of small limitations in the PHP support - not everything which is in the
specification can be done - and these limitations are summarised in a
later section.
