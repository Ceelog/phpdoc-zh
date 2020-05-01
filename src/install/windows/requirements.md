Install Requirements
--------------------

PHP 5.5+ require at least Windows 2008/Vista, or 2008r2, 2012, 2012r2,
2016 or 7, 8, 8.1, 10. Either 32-Bit or 64-bit (aka X86 or X64. PHP does
not run on Windows RT/WOA/ARM).

PHP requires the Visual C runtime(CRT). Many applications require that
so it may already be installed.

PHP 5.5 and 5.6 require VC CRT 11 (Visual Studio 2012). See:
<a href="https://www.microsoft.com/en-us/download/details.aspx?id=30679" class="link external">» https://www.microsoft.com/en-us/download/details.aspx?id=30679</a>

PHP 7.0+ requires VC CRT 14 (Visual Studio 2015). See:
<a href="https://www.microsoft.com/en-us/download/details.aspx?id=48145" class="link external">» https://www.microsoft.com/en-us/download/details.aspx?id=48145</a>

You MUST download the x86 CRT for PHP x86 builds and the x64 CRT for PHP
x64 builds.

If CRT is already installed, the installer will tell you that and not
change anything.

The CRT installer supports the /quiet and /norestart command-line
switches, so you can script running it.

VC11 CRT DLLs can be copied from your local machine to a remote
machine(a \`Copy Deployment\` installation) instead of running the
installer on the remote machine (such as a web server you have
restricted access to). See:
http://www.sitepoint.com/install-php53-windows/

VC14 CRT does not support a \`Copy Deployment\` installation. VC14 CRT
has many more DLLs(most in files with names starting with api-\*). If
you can find them all and copy them, it will also work (try a tool like
Resource Hacker to get a list of all the DLLs to copy).
