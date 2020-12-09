Enchant spelling library
========================

**目录**

-   [简介](/intro/enchant.html)
-   [安装／配置](/enchant/setup.html)
    -   [需求](/enchant/setup.html#需求)
    -   [安装](/enchant/setup.html#安装)
    -   [运行时配置](/enchant/setup.html#运行时配置)
    -   [资源类型](/enchant/setup.html#资源类型)
-   [预定义常量](/enchant/constants.html)
-   [范例](/enchant/examples.html)
-   [Enchant 函数](/ref/enchant.html)
    -   [enchant\_broker\_describe](/ref/enchant.html#enchant_broker_describe)
        — Enumerates the Enchant providers
    -   [enchant\_broker\_dict\_exists](/ref/enchant.html#enchant_broker_dict_exists)
        — Whether a dictionary exists or not. Using non-empty tag
    -   [enchant\_broker\_free\_dict](/ref/enchant.html#enchant_broker_free_dict)
        — Free a dictionary resource
    -   [enchant\_broker\_free](/ref/enchant.html#enchant_broker_free) —
        Free the broker resource and its dictionaries
    -   [enchant\_broker\_get\_dict\_path](/ref/enchant.html#enchant_broker_get_dict_path)
        — Get the directory path for a given backend
    -   [enchant\_broker\_get\_error](/ref/enchant.html#enchant_broker_get_error)
        — Returns the last error of the broker
    -   [enchant\_broker\_init](/ref/enchant.html#enchant_broker_init) —
        Create a new broker object capable of requesting
    -   [enchant\_broker\_list\_dicts](/ref/enchant.html#enchant_broker_list_dicts)
        — Returns a list of available dictionaries
    -   [enchant\_broker\_request\_dict](/ref/enchant.html#enchant_broker_request_dict)
        — Create a new dictionary using a tag
    -   [enchant\_broker\_request\_pwl\_dict](/ref/enchant.html#enchant_broker_request_pwl_dict)
        — Creates a dictionary using a PWL file
    -   [enchant\_broker\_set\_dict\_path](/ref/enchant.html#enchant_broker_set_dict_path)
        — Set the directory path for a given backend
    -   [enchant\_broker\_set\_ordering](/ref/enchant.html#enchant_broker_set_ordering)
        — Declares a preference of dictionaries to use for the language
    -   [enchant\_dict\_add\_to\_personal](/ref/enchant.html#enchant_dict_add_to_personal)
        — Add a word to personal word list
    -   [enchant\_dict\_add\_to\_session](/ref/enchant.html#enchant_dict_add_to_session)
        — Add 'word' to this spell-checking session
    -   [enchant\_dict\_check](/ref/enchant.html#enchant_dict_check) —
        Check whether a word is correctly spelled or not
    -   [enchant\_dict\_describe](/ref/enchant.html#enchant_dict_describe)
        — Describes an individual dictionary
    -   [enchant\_dict\_get\_error](/ref/enchant.html#enchant_dict_get_error)
        — Returns the last error of the current spelling-session
    -   [enchant\_dict\_is\_in\_session](/ref/enchant.html#enchant_dict_is_in_session)
        — Whether or not 'word' exists in this spelling-session
    -   [enchant\_dict\_quick\_check](/ref/enchant.html#enchant_dict_quick_check)
        — Check the word is correctly spelled and provide suggestions
    -   [enchant\_dict\_store\_replacement](/ref/enchant.html#enchant_dict_store_replacement)
        — Add a correction for a word
    -   [enchant\_dict\_suggest](/ref/enchant.html#enchant_dict_suggest)
        — Will return a list of values if any of those pre-conditions
        are not met
-   [EnchantBroker](/class/enchantbroker.html) — The EnchantBroker class
-   [EnchantDictionary](/class/enchantdictionary.html) — The
    EnchantDictionary class

简介
----

A fully opaque class which replaces *enchant\_broker* resources as of
PHP 8.0.0.

类摘要
------

**EnchantBroker**

<span class="ooclass"> <span class="modifier">final</span> class
**EnchantBroker** </span> {

}

简介
----

A fully opaque class which replaces *enchant\_dict* resources as of PHP
8.0.0.

类摘要
------

**EnchantDictionary**

<span class="ooclass"> <span class="modifier">final</span> class
**EnchantDictionary** </span> {

}
