This extension offers a PHP interface to the <span
class="productname">YAZ</span> toolkit that implements the
<a href="http://www.loc.gov/z3950/agency/" class="link external">» Z39.50 Protocol for Information Retrieval</a>.
With this extension you can easily implement a Z39.50 origin (client)
that searches or scans Z39.50 targets (servers) in parallel.

The module hides most of the complexity of Z39.50 so it should be fairly
easy to use. It supports persistent stateless connections very similar
to those offered by the various RDB APIs that are available for PHP.
This means that sessions are stateless but shared among users, thus
saving the connect and initialize phase steps in most cases.

<span class="productname">YAZ</span> is available at
<a href="http://www.indexdata.dk/yaz/" class="link external">» http://www.indexdata.dk/yaz/</a>.
You can find news information, example scripts, etc. for this extension
at
<a href="http://www.indexdata.dk/phpyaz/" class="link external">» http://www.indexdata.dk/phpyaz/</a>.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.0.0.
