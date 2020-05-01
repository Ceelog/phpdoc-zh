范例
====

**目录**

-   [Expect Usage
    Examples](/expect/examples.html#Expect%20Usage%20Examples)

Expect Usage Examples
---------------------

**示例 \#1 Expect Usage Example**

This example connects to the remote host via SSH, and prints the remote
uptime.

``` php
<?php
ini_set("expect.loguser", "Off");

$stream = fopen("expect://ssh root@remotehost uptime", "r");

$cases = array (
    array (0 => "password:", 1 => PASSWORD)
);

switch (expect_expectl ($stream, $cases)) {
    case PASSWORD:
        fwrite ($stream, "password\n");
        break;
 
    default:
        die ("Error was occurred while connecting to the remote host!\n");
}

while ($line = fgets($stream)) {
      print $line;
}
fclose ($stream);
?>
```

The following example connects to the remote host, determines whether
installed OS is for 32 or 64 bit, then runs update for specific package.

**示例 \#2 Another Expect Usage Example**

``` php
<?php
ini_set("expect.timeout", -1);
ini_set("expect.loguser", "Off");

$stream = expect_popen("ssh root@remotehost");

while (true) {
    switch (expect_expectl ($stream, array (
            array ("password:", PASSWORD), // SSH is asking for password
            array ("yes/no)?", YESNO), // SSH is asking whether to store the host entry
            array ("~$ ", SHELL, EXP_EXACT), // We've got the shell!
    ))) {
        case PASSWORD:
            fwrite ($stream, "secret\n");
            break;

        case YESNO:
            fwrite ($stream, "yes\n");
            break;

        case SHELL:
            fwrite ($stream, "uname -a\n");
            while (true) {
                    switch (expect_expectl ($stream, array (
                            array ("~$ ", SHELL, EXP_EXACT), // We've got the shell!
                            array ("^Linux.*$", UNAME, EXP_REGEXP), // uname -a output
                    ), $match)) {
                        case UNAME:
                            $uname .= $match[0];
                            break;

                        case SHELL:
                            // Run update:
                            if (strstr ($uname, "x86_64")) {
                                    fwrite ($stream, "rpm -Uhv http://mirrorsite/somepath/some_64bit.rpm\n");
                            } else {
                                    fwrite ($stream, "rpm -Uhv http://mirrorsite/somepath/some_32bit.rpm\n");
                            }
                            fwrite ($stream, "exit\n");
                            break 2;

                        case EXP_TIMEOUT:
                        case EXP_EOF:
                            break 2;

                        default:
                            die ("Error has occurred!\n");
                    }
            }
            break 2;

        case EXP_TIMEOUT:
        case EXP_EOF:
            break 2;

        default:
            die ("Error has occurred!\n");
    }
}

fclose ($stream);
?>
```
