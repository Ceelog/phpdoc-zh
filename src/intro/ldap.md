LDAP is the Lightweight Directory Access Protocol, and is a protocol
used to access "Directory Servers". The Directory is a special kind of
database that holds information in a tree structure.

The concept is similar to your hard disk directory structure, except
that in this context, the root directory is "The world" and the first
level subdirectories are "countries". Lower levels of the directory
structure contain entries for companies, organisations or places, while
yet lower still we find directory entries for people, and perhaps
equipment or documents.

To refer to a file in a subdirectory on your hard disk, you might use
something like:

``` literallayout
   /usr/local/myapp/docs
  
```

The forwards slash marks each division in the reference, and the
sequence is read from left to right.

The equivalent to the fully qualified file reference in LDAP is the
"distinguished name", referred to simply as "dn". An example dn might
be:

``` literallayout
   cn=John Smith,ou=Accounts,o=My Company,c=US
  
```

The comma marks each division in the reference, and the sequence is read
from right to left. You would read this dn as:

``` literallayout
   country = US
   organization = My Company
   organizationalUnit = Accounts
   commonName = John Smith
  
```

In the same way as there are no hard rules about how you organise the
directory structure of a hard disk, a directory server manager can set
up any structure that is meaningful for the purpose. However, there are
some conventions that are used. The message is that you can not write
code to access a directory server unless you know something about its
structure, any more than you can use a database without some knowledge
of what is available.

Lots of information about LDAP can be found at

-   <a href="https://wiki.mozilla.org/Directory" class="link external">» Mozilla</a>

-   <a href="http://www.openldap.org/" class="link external">» OpenLDAP Project</a>

-   Internet Engineering Taskforce RFCs
    <a href="http://www.faqs.org/rfcs/rfcrfc4510" class="link external">» 4510</a>
    through
    <a href="http://www.faqs.org/rfcs/rfcrfc4519" class="link external">» 4519</a>.

The Netscape SDK contains a helpful
<a href="https://wiki.mozilla.org/Mozilla_LDAP_SDK_Programmer%27s_Guide" class="link external">» Programmer's Guide</a>
in HTML format.
