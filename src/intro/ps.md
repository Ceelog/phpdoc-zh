This module allows to create PostScript documents. It has many
similarities with the pdf extension. Actually the API is almost
identical and one can in many cases just replace the prefix of each
function from pdf\_ to ps\_. This also works for functions which has no
meaning in the PostScript document (like adding hyperlinks) but will
have an effect if the document is converted to PDF.

Documents created by this extension are sometimes even superior to
documents created with the pdf extension, because pslib's text rendering
functions can handle kerning, hyphenation and ligatures which results in
much better output of boxed text.
