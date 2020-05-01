These functions allow for arbitrary-length integers to be worked with
using the GNU MP library.

> **Note**:
>
> Most GMP functions accept GMP number arguments. These are shown in
> this documentation as <span class="classname">GMP</span> objects.
> However, note that PHP 5.5 and earlier represented GMP numbers as
> <span class="type">resource</span>s. Most of these functions will also
> accept numeric and string arguments, so long as it is possible to
> convert the latter to a number. Also, if there is a more performant
> function that can operate on the arguments (integers only), then it
> will be used instead (this is done transparently). See also the <span
> class="function">gmp\_init</span> function.

> **Note**:
>
> From PHP 5.6 onwards, the
> <a href="/language/operators/arithmetic.html" class="link">arithmetic</a>,
> <a href="/language/operators/bitwise.html" class="link">bitwise</a>,
> and
> <a href="/language/operators/comparison.html" class="link">comparison</a>
> operators may be used with the <span class="classname">GMP</span>
> objects returned from <span class="function">gmp\_init</span> and
> other GMP functions.

**Warning**

Large integers must be specified as strings - otherwise, PHP will coerce
them to floats, resulting in a loss of precision.

> **Note**: <span class="simpara"> This extension is available on
> Windows platforms since PHP 5.1.0. </span>
