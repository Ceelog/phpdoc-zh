预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Each *TIDY\_TAG\_XXX* represents a HTML tag. For example,
**`TIDY_TAG_A`** represents a *"\<a href="XX"\>link\</a\>"* tag.

The following constants are defined:

| Constant                  | Notes                                              |
|---------------------------|----------------------------------------------------|
| **`TIDY_TAG_UNKNOWN`**    |                                                    |
| **`TIDY_TAG_A`**          |                                                    |
| **`TIDY_TAG_ABBR`**       |                                                    |
| **`TIDY_TAG_ACRONYM`**    |                                                    |
| **`TIDY_TAG_ALIGN`**      |                                                    |
| **`TIDY_TAG_APPLET`**     |                                                    |
| **`TIDY_TAG_AREA`**       |                                                    |
| **`TIDY_TAG_ARTICLE`**    | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_ASIDE`**      | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_AUDIO`**      | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_B`**          |                                                    |
| **`TIDY_TAG_BASE`**       |                                                    |
| **`TIDY_TAG_BASEFONT`**   |                                                    |
| **`TIDY_TAG_BDI`**        | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_BDO`**        |                                                    |
| **`TIDY_TAG_BGSOUND`**    |                                                    |
| **`TIDY_TAG_BIG`**        |                                                    |
| **`TIDY_TAG_BLINK`**      |                                                    |
| **`TIDY_TAG_BLOCKQUOTE`** |                                                    |
| **`TIDY_TAG_BODY`**       |                                                    |
| **`TIDY_TAG_BR`**         |                                                    |
| **`TIDY_TAG_BUTTON`**     |                                                    |
| **`TIDY_TAG_CANVAS`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_CAPTION`**    |                                                    |
| **`TIDY_TAG_CENTER`**     |                                                    |
| **`TIDY_TAG_CITE`**       |                                                    |
| **`TIDY_TAG_CODE`**       |                                                    |
| **`TIDY_TAG_COL`**        |                                                    |
| **`TIDY_TAG_COLGROUP`**   |                                                    |
| **`TIDY_TAG_COMMAND`**    | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_COMMENT`**    |                                                    |
| **`TIDY_TAG_DATALIST`**   | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_DD`**         |                                                    |
| **`TIDY_TAG_DEL`**        |                                                    |
| **`TIDY_TAG_DETAILS`**    | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_DFN`**        |                                                    |
| **`TIDY_TAG_DIALOG`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_DIR`**        |                                                    |
| **`TIDY_TAG_DIV`**        |                                                    |
| **`TIDY_TAG_DL`**         |                                                    |
| **`TIDY_TAG_DT`**         |                                                    |
| **`TIDY_TAG_EM`**         |                                                    |
| **`TIDY_TAG_EMBED`**      |                                                    |
| **`TIDY_TAG_FIELDSET`**   |                                                    |
| **`TIDY_TAG_FIGCAPTION`** | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_FIGURE`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_FONT`**       |                                                    |
| **`TIDY_TAG_FOOTER`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_FORM`**       |                                                    |
| **`TIDY_TAG_FRAME`**      |                                                    |
| **`TIDY_TAG_FRAMESET`**   |                                                    |
| **`TIDY_TAG_H1`**         |                                                    |
| **`TIDY_TAG_H2`**         |                                                    |
| **`TIDY_TAG_H3`**         |                                                    |
| **`TIDY_TAG_H4`**         |                                                    |
| **`TIDY_TAG_H5`**         |                                                    |
| **`TIDY_TAG_H6`**         |                                                    |
| **`TIDY_TAG_HEAD`**       |                                                    |
| **`TIDY_TAG_HEADER`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_HGROUP`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_HR`**         |                                                    |
| **`TIDY_TAG_HTML`**       |                                                    |
| **`TIDY_TAG_I`**          |                                                    |
| **`TIDY_TAG_IFRAME`**     |                                                    |
| **`TIDY_TAG_ILAYER`**     |                                                    |
| **`TIDY_TAG_IMG`**        |                                                    |
| **`TIDY_TAG_INPUT`**      |                                                    |
| **`TIDY_TAG_INS`**        |                                                    |
| **`TIDY_TAG_ISINDEX`**    |                                                    |
| **`TIDY_TAG_KBD`**        |                                                    |
| **`TIDY_TAG_KEYGEN`**     |                                                    |
| **`TIDY_TAG_LABEL`**      |                                                    |
| **`TIDY_TAG_LAYER`**      |                                                    |
| **`TIDY_TAG_LEGEND`**     |                                                    |
| **`TIDY_TAG_LI`**         |                                                    |
| **`TIDY_TAG_LINK`**       |                                                    |
| **`TIDY_TAG_LISTING`**    |                                                    |
| **`TIDY_TAG_MAIN`**       | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_MAP`**        |                                                    |
| **`TIDY_TAG_MARK`**       | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_MARQUEE`**    |                                                    |
| **`TIDY_TAG_MENU`**       |                                                    |
| **`TIDY_TAG_MENUITEM`**   | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_META`**       |                                                    |
| **`TIDY_TAG_METER`**      | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_MULTICOL`**   |                                                    |
| **`TIDY_TAG_NAV`**        | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_NOBR`**       |                                                    |
| **`TIDY_TAG_NOEMBED`**    |                                                    |
| **`TIDY_TAG_NOFRAMES`**   |                                                    |
| **`TIDY_TAG_NOLAYER`**    |                                                    |
| **`TIDY_TAG_NOSAVE`**     |                                                    |
| **`TIDY_TAG_NOSCRIPT`**   |                                                    |
| **`TIDY_TAG_OBJECT`**     |                                                    |
| **`TIDY_TAG_OL`**         |                                                    |
| **`TIDY_TAG_OPTGROUP`**   |                                                    |
| **`TIDY_TAG_OPTION`**     |                                                    |
| **`TIDY_TAG_OUTPUT`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_P`**          |                                                    |
| **`TIDY_TAG_PARAM`**      |                                                    |
| **`TIDY_TAG_PLAINTEXT`**  |                                                    |
| **`TIDY_TAG_PRE`**        |                                                    |
| **`TIDY_TAG_PROGRESS`**   | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_Q`**          |                                                    |
| **`TIDY_TAG_RB`**         |                                                    |
| **`TIDY_TAG_RBC`**        |                                                    |
| **`TIDY_TAG_RP`**         |                                                    |
| **`TIDY_TAG_RT`**         |                                                    |
| **`TIDY_TAG_RTC`**        |                                                    |
| **`TIDY_TAG_RUBY`**       |                                                    |
| **`TIDY_TAG_S`**          |                                                    |
| **`TIDY_TAG_SAMP`**       |                                                    |
| **`TIDY_TAG_SCRIPT`**     |                                                    |
| **`TIDY_TAG_SECTION`**    | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_SELECT`**     |                                                    |
| **`TIDY_TAG_SERVER`**     |                                                    |
| **`TIDY_TAG_SERVLET`**    |                                                    |
| **`TIDY_TAG_SMALL`**      |                                                    |
| **`TIDY_TAG_SOURCE`**     | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_SPACER`**     |                                                    |
| **`TIDY_TAG_SPAN`**       |                                                    |
| **`TIDY_TAG_STRIKE`**     |                                                    |
| **`TIDY_TAG_STRONG`**     |                                                    |
| **`TIDY_TAG_STYLE`**      |                                                    |
| **`TIDY_TAG_SUB`**        |                                                    |
| **`TIDY_TAG_SUMMARY`**    | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_SUP`**        |                                                    |
| **`TIDY_TAG_TABLE`**      |                                                    |
| **`TIDY_TAG_TBODY`**      |                                                    |
| **`TIDY_TAG_TD`**         |                                                    |
| **`TIDY_TAG_TEMPLATE`**   | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_TEXTAREA`**   |                                                    |
| **`TIDY_TAG_TFOOT`**      |                                                    |
| **`TIDY_TAG_TH`**         |                                                    |
| **`TIDY_TAG_THEAD`**      |                                                    |
| **`TIDY_TAG_TIME`**       | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_TITLE`**      |                                                    |
| **`TIDY_TAG_TR`**         |                                                    |
| **`TIDY_TAG_TRACK`**      | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_TT`**         |                                                    |
| **`TIDY_TAG_U`**          |                                                    |
| **`TIDY_TAG_UL`**         |                                                    |
| **`TIDY_TAG_VAR`**        |                                                    |
| **`TIDY_TAG_VIDEO`**      | Added in libtidy 5.0.0. Available as of PHP 7.4.0. |
| **`TIDY_TAG_WBR`**        |                                                    |
| **`TIDY_TAG_XMP`**        |                                                    |

| constant                     | description            |
|------------------------------|------------------------|
| **`TIDY_NODETYPE_ROOT`**     | root node              |
| **`TIDY_NODETYPE_DOCTYPE`**  | doctype                |
| **`TIDY_NODETYPE_COMMENT`**  | HTML comment           |
| **`TIDY_NODETYPE_PROCINS`**  | Processing Instruction |
| **`TIDY_NODETYPE_TEXT`**     | Text                   |
| **`TIDY_NODETYPE_START`**    | start tag              |
| **`TIDY_NODETYPE_END`**      | end tag                |
| **`TIDY_NODETYPE_STARTEND`** | empty tag              |
| **`TIDY_NODETYPE_CDATA`**    | CDATA                  |
| **`TIDY_NODETYPE_SECTION`**  | XML section            |
| **`TIDY_NODETYPE_ASP`**      | ASP code               |
| **`TIDY_NODETYPE_JSTE`**     | JSTE code              |
| **`TIDY_NODETYPE_PHP`**      | PHP code               |
| **`TIDY_NODETYPE_XMLDECL`**  | XML declaration        |
