The parle extension provides general purpose lexing and parsing
facilities. The implementation is based on
<a href="http://www.benhanson.net/" class="link external">» Ben Hanson</a>'s
libraries and requires a
<a href="http://en.cppreference.com/w/cpp/compiler_support" class="link external">» C++14</a>
capable compiler. The lexer is based on the regex matching, the parser
is LALR(1). Lexers and parsers are generated on the fly and can be used
immediately after they've been finalized. Parle deals with parsing and
lexing, the appropriate data structures representation and processing
are the implementer's task. Serialization and code generation are not
supported by the extension, yet.

Lexer analysis is a process of splitting a character sequence into a
list of lexemes. The lexeme list can be then used for the syntax
analysis against a formal grammar. These operations are also known as
lexing and parsing. This documentation doesn't aim to provide an
exhaustive information on lexing and parsing. Good information in this
regard is available on the numerous resources on the net. Several usage
examples are included, to show the functionality. The extension is
useful for PHP programmers both willing to learn or to utilize parsing
and lexing. State machines and grammar parsing don't have to be
implemented manually, these complex tasks are taken away by parle.
Thanks to that, the development can be focused on the actual problem
solving.

The common use case for parle is, when a data format is too complex to
be handled by the regex matching with PCRE. The practical application is
herewith wide. Be it a specific data format, a behavior modification of
existing functions, even an own programming language and beyond. The
helper methods such as <span
class="methodname">Parle\\Lexer::dump</span> to inspect the generated
state machine, or <span class="methodname">Parle\\Parser::dump</span> to
inspect the generated grammar, are useful. The method <span
class="methodname">Parle\\Parser::trace</span> can also be used to track
the parsing operation.
