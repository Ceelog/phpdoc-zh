xdiff extension enables you to create and apply patch files containing
differences between different revisions of files.

This extension supports two modes of operation - on strings and on
files, as well as two different patch formats - unified and binary.
Unified patches are excellent for text files as they are human-readable
and easy to review. For binary files like archives or images, binary
patches will be adequate choice as they are binary safe and handle
non-printable characters well.

Starting from version 1.5.0 there are two different sets of functions
for generating binary patches. New functions - <span
class="function">xdiff\_string\_rabdiff</span> and <span
class="function">xdiff\_file\_rabdiff</span> generate output compatible
with older functions but are typically faster and generate smaller
results. For more details about methods of generating binary patches and
differences between them, please check
<a href="http://www.xmailserver.org/xdiff-lib.html" class="link external">» libxdiff</a>
website.

This extension uses libxdiff to implement these functions. Please see
<a href="http://www.xmailserver.org/xdiff-lib.html" class="link external">» http://www.xmailserver.org/xdiff-lib.html</a>
for more information.
