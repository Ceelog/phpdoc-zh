Forms Data Format (FDF) is a format for handling forms within PDF
documents. You should read the documentation at
<a href="http://www.adobe.com/devnet/acrobat/fdftoolkit.html" class="link external">» http://www.adobe.com/devnet/acrobat/fdftoolkit.html</a>
for more information on what FDF is and how it is used in general.

The general idea of FDF is similar to HTML forms. The difference is
basically the format how data is transmitted to the server when the
submit button is pressed (this is actually the Form Data Format) and the
format of the form itself (which is the Portable Document Format, PDF).
Processing the FDF data is one of the features provided by the fdf
functions. But there is more. One may as well take an existing PDF form
and populated the input fields with data without modifying the form
itself. In such a case one would create a FDF document (<span
class="function">fdf\_create</span>) set the values of each input field
(<span class="function">fdf\_set\_value</span>) and associate it with a
PDF form (<span class="function">fdf\_set\_file</span>). Finally it has
to be sent to the browser with MimeType *application/vnd.fdf*. The
Acrobat reader plugin of your browser recognizes the MimeType, reads the
associated PDF form and fills in the data from the FDF document.

If you look at an FDF-document with a text editor you will find a
catalogue object with the name *FDF*. Such an object may contain a
number of entries like *Fields*, *F*, *Status* etc.. The most commonly
used entries are *Fields* which points to a list of input fields, and
*F* which contains the filename of the PDF-document this data belongs
to. Those entries are referred to in the FDF documentation as /F-Key or
/Status-Key. Modifying this entries is done by functions like <span
class="function">fdf\_set\_file</span> and <span
class="function">fdf\_set\_status</span>. Fields are modified with <span
class="function">fdf\_set\_value</span>, <span
class="function">fdf\_set\_opt</span> etc..
