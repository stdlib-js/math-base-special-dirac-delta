<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Dirac Delta

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Evaluate the [Dirac delta function][dirac-delta-function].

<section class="intro">

The [Dirac delta function][dirac-delta-function] may be loosely defined as

<!-- <equation class="equation" label="eq:dirac_delta" align="center" raw="\delta = \begin{cases} \infty & \textrm{if}\ x = 0 \\ 0 & \textrm{if}\ x \neq 0\end{cases}" alt="Dirac delta function."> -->

```math
\delta = \begin{cases} \infty & \textrm{if}\ x = 0 \\ 0 & \textrm{if}\ x \neq 0\end{cases}
```

<!-- <div class="equation" align="center" data-raw-text="\delta = \begin{cases} \infty &amp; \textrm{if}\ x = 0 \\ 0 &amp; \textrm{if}\ x \neq 0\end{cases}" data-equation="eq:dirac_delta">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/dirac-delta/docs/img/equation_dirac_delta.svg" alt="Dirac delta function.">
    <br>
</div> -->

<!-- </equation> -->

and is constrained to satisfy the identity

<!-- <equation class="equation" label="eq:dirac_delta_integral" align="center" raw="\int^{+\infty}_{-\infty} \delta(x)\ dx = 1" alt="Dirac delta function integral."> -->

```math
\int^{+\infty}_{-\infty} \delta(x)\ dx = 1
```

<!-- <div class="equation" align="center" data-raw-text="\int^{+\infty}_{-\infty} \delta(x)\ dx = 1" data-equation="eq:dirac_delta_integral">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/dirac-delta/docs/img/equation_dirac_delta_integral.svg" alt="Dirac delta function integral.">
    <br>
</div> -->

<!-- </equation> -->

Note that the [Dirac delta function][dirac-delta-function] is **not** a function in the traditional sense, as any real-valued function which is zero everywhere except at a single point, must have an integral equal to `0`.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-dirac-delta
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var diracDelta = require( '@stdlib/math-base-special-dirac-delta' );
```

#### diracDelta( x )

Evaluates the [Dirac delta function][dirac-delta-function].

```javascript
var v = diracDelta( 0.0 );
// returns Infinity

v = diracDelta( 3.14 );
// returns 0.0

v = diracDelta( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var uniform = require( '@stdlib/random-array-uniform' );
var logEachMap = require( '@stdlib/console-log-each-map' );
var diracDelta = require( '@stdlib/math-base-special-dirac-delta' );

var opts = {
    'dtype': 'float64'
};
var x = uniform( 100, -1.0, 1.0, opts );

logEachMap( 'dirac(%0.4f) = %0.4f', x, diracDelta );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/math/base/special/dirac_delta.h"
```

#### stdlib_base_dirac_delta( x )

Evaluates the [Dirac delta function][dirac-delta-function].

```c
double x = stdlib_base_dirac_delta( 0.0 );
// returns Infinity

x = stdlib_base_dirac_delta( 3.14 );
// returns 0.0
```

The function accepts the following arguments:

-   **x**: `[in] double` input value.

```c
double stdlib_base_dirac_delta( const double x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/special/dirac_delta.h"
#include <stdlib.h>
#include <stdio.h>

int main( void ) {
    const double x[] = { -1.0, -0.5, 0.0, 0.5, 1.0, 3.14, 2.0 };

    double v;
    int i;
    for ( i = 0; i < 7; i++ ) {
        v = stdlib_base_dirac_delta( x[ i ] );
        printf( "dirac(%lf) = %lf\n", x[ i ], v );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/special/kronecker-delta`][@stdlib/math/base/special/kronecker-delta]</span><span class="delimiter">: </span><span class="description">evaluate the Kronecker delta.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-dirac-delta.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-dirac-delta

[test-image]: https://github.com/stdlib-js/math-base-special-dirac-delta/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-dirac-delta/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-dirac-delta?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-dirac-delta.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-dirac-delta/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-dirac-delta/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-dirac-delta/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-dirac-delta/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-dirac-delta/main/LICENSE

[dirac-delta-function]: https://en.wikipedia.org/wiki/Dirac_delta_function

<!-- <related-links> -->

[@stdlib/math/base/special/kronecker-delta]: https://github.com/stdlib-js/math-base-special-kronecker-delta

<!-- </related-links> -->

</section>

<!-- /.links -->
