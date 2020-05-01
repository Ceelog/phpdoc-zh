范例
====

**目录**

-   [Lexer examples](/parle/examples.html#Lexer%20examples)
-   [Parser examples](/parle/examples.html#Parser%20examples)

Lexer examples
--------------

**示例 \#1 Tokenize comma separated integer list**

``` php
<?php

use Parle\Token;
use Parle\Lexer;
use Parle\LexerException;

/* name => id */
$token = array(
        "COMMA" => 1,
        "CRLF" => 2,
        "DECIMAL" => 3,
);
/* id => name */
$tokenIdToName = array_flip($token);

$lex = new Lexer;
$lex->push("[\x2c]", $token["COMMA"]);
$lex->push("[\r][\n]", $token["CRLF"]);
$lex->push("[\d]+", $token["DECIMAL"]);
$lex->build();

$in = "0,1,2\r\n3,42,5\r\n6,77,8\r\n";

$lex->consume($in);

do {
        $lex->advance();
        $tok = $lex->getToken();

        if (Token::UNKNOWN == $tok->id) {
                throw new LexerException("Unknown token '{$tok->value}' at offset {$lex->marker}.");
        }

        echo "TOKEN: ", $tokenIdToName[$tok->id], PHP_EOL;
} while (Token::EOI != $tok->id);
```

**示例 \#2 Tokenize assign statement**

``` php
<?php

use Parle\{Token, Lexer};

$lex = new Lexer;

$lex->push("\$[a-zA-Z_][a-zA-Z0-9_]*", 1);
$lex->push("=", 2);
$lex->push("\d+", 3);
$lex->push(";", 4);

$lex->build();

$lex->consume('$x = 42; $y = 24;');


do {
    $lex->advance();
    $tok = $lex->getToken();
    var_dump($tok);
} while (Token::EOI != $tok->id);
```

Parser examples
---------------

**示例 \#1 Simple calculator**

``` php
<?php 

use Parle\{Parser, ParserException, Lexer, Token};

$p = new Parser;
$p->token("INTEGER");
$p->left("'+' '-' '*' '/'");

$p->push("start", "exp");
$prod_add = $p->push("exp", "exp '+' exp");
$prod_sub = $p->push("exp", "exp '-' exp");
$prod_mul = $p->push("exp", "exp '*' exp");
$prod_div = $p->push("exp", "exp '/' exp");
$p->push("exp", "INTEGER"); /* Production index unused. */

$p->build();

$lex = new Lexer;
$lex->push("[+]", $p->tokenId("'+'"));
$lex->push("[-]", $p->tokenId("'-'"));
$lex->push("[*]", $p->tokenId("'*'"));
$lex->push("[/]", $p->tokenId("'/'"));
$lex->push("\\d+", $p->tokenId("INTEGER"));
$lex->push("\\s+", Token::SKIP);

$lex->build();

$exp = array(
    "1 + 1",
    "33 / 10",
    "100 * 45",
    "17 - 45",
);

foreach ($exp as $in) {
    if (!$p->validate($in, $lex)) {
        throw new ParserException("Failed to validate input");
    }

    $p->consume($in, $lex);

    while (Parser::ACTION_ERROR != $p->action && Parser::ACTION_ACCEPT != $p->action) {
        switch ($p->action) {
            case Parser::ACTION_ERROR:
                throw new ParserException("Parser error");
                break;
            case Parser::ACTION_SHIFT:
            case Parser::ACTION_GOTO:
            case Parser::ACTION_ACCEPT:
                break;
            case Parser::ACTION_REDUCE:
                switch ($p->reduceId) {
                    case $prod_add:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l + $r = " . ($l + $r) . "\n";
                        break;
                    case $prod_sub:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l - $r = " . ($l - $r) . "\n";
                        break;
                    case $prod_mul:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                        echo "$l * $r = " . ($l * $r) . "\n";
                        break;
                    case $prod_div:
                        $l = $p->sigil(0);
                        $r = $p->sigil(2);
                    echo "$l / $r = " . ($l / $r) . "\n";
                        break;
            }
            break;
        }
        $p->advance();
    }
}
```

**示例 \#2 Parse words out from a sentence**

``` php
<?php

use Parle\{Lexer, Token, Parser, ParserException};

$p = new Parser;
$p->token("WORD");
$p->push("START", "SENTENCE");
$p->push("SENTENCE", "WORDS");
$prod_word_0 = $p->push("WORDS", "WORDS WORD");
$prod_word_1 = $p->push("WORDS", "WORD");
$p->build();

$lex = new Lexer;
$lex->push("[^\s]{-}[\.,\:\;\?]+", $p->tokenId("WORD"));
$lex->push("[\s\.,\:\;\?]+", Token::SKIP);
$lex->build();

$in = "Dis-moi où est ton papa?";
$p->consume($in, $lex);
do {
    switch ($p->action) {
    case Parser::ACTION_ERROR:
        throw new ParserException("Error");
        break;
    case Parser::ACTION_SHIFT:
    case Parser::ACTION_GOTO:
        /* var_dump($p->trace());*/
        break;
    case Parser::ACTION_REDUCE:
        $rid = $p->reduceId();
        if ($rid == $prod_word_1) {
            var_dump($p->sigil(0));
        } if ($rid == $prod_word_0) {
            var_dump($p->sigil(1));
        }
        break;
    }
    $p->advance();
} while (Parser::ACTION_ACCEPT != $p->action);
```
