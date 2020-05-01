Packaging and distribution
--------------------------

### Creating a package

PDO drivers are released via PECL; all the usual rules for PECL
extensions apply. Packaging is accomplished by creating a valid
`package.xml` file and then running:

    $ pecl package

This will create a tarball named `PDO_SKEL-X.Y.Z.tgz`.

Before releasing the package, you should test that it builds correctly;
if you've made a mistake in your `config.m4` or `package.xml` files, the
package may not function correctly. You can test the build, without
installing anything, using the following invocation:

    $ pecl build package.xml

Once this is proven to work, you can test installation:

    $ pecl package
    $ sudo pecl install PDO_SKEL-X.Y.X.tgz

Full details about `package.xml` can be found in the PEAR Programmer's
documentation
(<a href="https://pear.php.net/manual/" class="link external">» https://pear.php.net/manual/</a>).

### Releasing the package

A PDO driver is released via the PHP Extension Community Library (PECL).
Information about PECL can be found at
<a href="https://pecl.php.net/" class="link external">» https://pecl.php.net/</a>.
