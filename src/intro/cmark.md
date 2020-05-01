This extension provides access to the reference implementation of
CommonMark, a rationalized version of Markdown syntax with a
specification.

##### Parsing:

The CommonMark extension provides a simple parsing API:

<span class="type">CommonMark\\Node</span> <span
class="methodname">CommonMark\\Parse</span> ( <span
class="methodparam"><span class="type">string</span> `$content`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$options`</span> \] )

##### Rendering:

The CommonMark extension provides simple rendering API that supports
multiple formats:

<span class="type">string</span> <span
class="methodname">CommonMark\\Render</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\HTML</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\XML</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \] )

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\Man</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

<span class="type">string</span> <span
class="methodname">CommonMark\\Render\\Latex</span> ( <span
class="methodparam"><span class="type">CommonMark\\Node</span>
`$node`</span> \[, <span class="methodparam"><span
class="type">int</span> `$options`</span> \[, <span
class="methodparam"><span class="type">int</span> `$width`</span> \]\] )

##### AST:

The CommonMark extension implements visitation for CommonMark\\Node
objects:

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">CommonMark\\Node::accept</span> ( <span
class="methodparam"><span
class="type">CommonMark\\Interfaces\\IVisitor</span> `$visitor`</span> )

##### CQL:

The CommonMark extension provides an interface to CQL, CommonMark Query
Language:

<span class="modifier">public</span> <span
class="methodname">CommonMark\\CQL::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$query`</span> )
