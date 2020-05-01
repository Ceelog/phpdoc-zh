Azure App Services
------------------

PHP is frequently used on Azure App Services (aka Microsoft Azure,
Windows Azure, Azure Web Apps).

Azure App Services manages pools of Windows Web Servers to host your web
application, as an alternative to managing your own web server on your
own Azure Compute VMs or other servers.

PHP is already enabled for your Azure App Services web site
automatically. In the Azure Portal, select your web site, and you can
choose which version of PHP to use. You may want to choose a newer
version than the default.

As such, PHP and extensions will run on Azure App Services just as it
will on other Windows servers. Much of the knowledgebase is also
portable, so see the
<a href="/install/windows/troubleshooting.html" class="link">Windows Troubleshooting Page</a>
too. However, the management interface for Azure App Services is
different:

-   Azure portal: create, edit settings and delete web sites.
    <a href="https://portal.azure.com/" class="link external">» Azure Portal</a>

-   Kudu Dashboard: \[your web site name\].azurewebsites.net Then, the
    Kudu dashboard is
    <a href="https://your_web_site_name.scm.azurewebsites.net/" class="link external">» https://[your web site name].scm.azurewebsites.net/</a>.
    The Dashboard gives you access to some debugging capabilities, file
    management and site extensions. Site extensions are an Azure
    mechanism to add extra programs, like PHP preview builds, to your
    web site.

-   You can not use IIS Manager, Server Manager, or RDP.

There is also a PHP SDK for programmatically using many Azure Services
from your PHP code. See
<a href="https://github.com/Azure/azure-sdk-for-php" class="link external">» Azure SDK for PHP</a>.

For more information, see
<a href="https://azure.microsoft.com/en-us/develop/php/" class="link external">» Azure PHP Developer Center</a>

### WinCache

WinCache is enabled by default on Azure App Services and it is
recommended that you leave it enabled. If you install your own build of
PHP, you should enable WinCache on that too.

### Custom PHP Build

You may upload your own PHP build to your D:\\Home (C:\\ is NOT
writable). Then in the Azure Portal, set SCRIPT\_PROCESSOR for .php to
the absolute path to php-cgi.exe file in your build.
