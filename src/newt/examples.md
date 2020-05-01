范例
====

**目录**

-   [Basic usage](/newt/examples.html#Basic%20usage)

Basic usage
-----------

This example is a PHP port of RedHat 'setup' utility dialog, executed in
text mode.

**示例 \#1 Newt Usage Example**

``` php
<?php
newt_init ();
newt_cls ();

newt_draw_root_text (0, 0, "Test Mode Setup Utility 1.12");
newt_push_help_line (null);
newt_draw_root_text (-30, 0, "(c) 1999-2002 RedHat, Inc");

newt_get_screen_size ($rows, $cols);

newt_open_window ($rows/2-17, $cols/2-10, 34, 17, "Choose a Tool");

$form = newt_form ();

$list = newt_listbox (3, 2, 10);

foreach (array (
    "Authentication configuration",
    "Firewall configuration",
    "Mouse configuration",
    "Network configuration",
    "Printer configuration",
    "System services") as $l_item)
{
    newt_listbox_add_entry ($list, $l_item, $l_item);
}

$b1 = newt_button (5, 12, "Run Tool");
$b2 = newt_button (21, 12, "Quit");

newt_form_add_component ($form, $list);
newt_form_add_components ($form, array($b1, $b2));

newt_refresh ();
newt_run_form ($form);

newt_pop_window ();
newt_pop_help_line ();
newt_finished ();
newt_form_destroy ($form);
?>
```
