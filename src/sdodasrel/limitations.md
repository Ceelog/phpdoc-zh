Limitations
===========

There are the following limitations in the current release of the
Relational DAS:

-   No support for nulls. There is no support for SQL NULL type. It is
    not legal to assign PHP NULL to a data object property and the
    Relational DAS will not write that back as a NULL to the database.
    If nulls are found in the database on a query, the property will
    remain unset.

-   Only two types of SDO relationship. The metadata described below
    allows the Relational DAS to model just two types of SDO
    relationship: multi-valued containment relationships and
    single-valued non-containment references. In SDO, whether a property
    describes a single- or multi-valued relationship, and whether it is
    containment or non-containment, are independent. The full range of
    possibilities that SDO allows cannot all be defined. There may be
    relationships that it would be useful to model but which the current
    implementation cannot manage. One example is a single-valued
    containment relationship.

-   No support for the full range of SDO data types. The Relational DAS
    defines all primitive properties in the SDO model as being of type
    string. SDO defines a richer set of types containing various
    integer, float, boolean and data and time types. String is adequate
    for the purposes of the Relational DAS since the combination of PHP,
    PDO and the database will ensure that values passed as strings will
    be converted to the proper type before being put in the database.
    This does affect some scenarios in which the Relational DAS has to
    work with a data graph that has come from or will go to a different
    DAS.

-   Only one foreign key per table. The metadata only provides the means
    to specify one foreign key per table. This foreign key may be mapped
    to one of the two types of SDO relationship supported. Obviously
    there are some scenarios that cannot be described under this
    limitation - it is not possible to have two non-containment
    references from one table to another for example.
