**Warning**

This extension has been deprecated as the PECL extension
<a href="/book/fileinfo.html" class="link">Fileinfo</a> provides the
same functionality (and more) in a much cleaner way.

The functions in this module try to guess the content type and encoding
of a file by looking for certain *magic* byte sequences at specific
positions within the file. While this is not a bullet proof approach the
heuristics used do a very good job.

This extension is derived from Apache mod\_mime\_magic, which is itself
based on the `file` command maintained by Ian F. Darwin. See the source
code for further historic and copyright information.
