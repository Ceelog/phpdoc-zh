COM is an acronym for *Component Object Model*; it is an object
orientated layer (and associated services) on top of DCE RPC (an open
standard) and defines a common calling convention that enables code
written in any language to call and interoperate with code written in
any other language (provided those languages are COM aware). Not only
can the code be written in any language, but it need not even be part of
the same executable; the code can be loaded from a DLL, be found in
another process running on the same machine, or, with DCOM (Distributed
COM), be found in another process on a remote machine, all without your
code even needing to know where a component resides.

There is a subset of COM known as OLE Automation which comprises a set
of COM interfaces that allow loose binding to COM objects, so that they
can be introspected and called at run-time without compile-time
knowledge of how the object works. The PHP COM extension utilizes the
OLE Automation interfaces to allow you to create and call compatible
objects from your scripts. Technically speaking, this should really be
called the "*OLE Automation Extension for PHP*", since not all COM
objects are OLE compatible.

Now, why would or should you use COM? COM is one of the main ways to
glue applications and components together on the Windows platform; using
COM you can launch Microsoft Word, fill in a document template and save
the result as a Word document and send it to a visitor of your web site.
You can also use COM to perform administrative tasks for your network
and to configure your IIS; these are just the most common uses; you can
do much more with COM.

Additionally, we support the instantiation and creation of .Net
assemblies using the COM interoperability layer provided by Microsoft.
