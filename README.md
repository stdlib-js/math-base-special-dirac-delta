<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Dirac Delta

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Evaluate the [Dirac delta function][dirac-delta-function].

<section class="intro">

The [Dirac delta function][dirac-delta-function] may be loosely defined as

<!-- <equation class="equation" label="eq:dirac_delta" align="center" raw="\delta = \begin{cases} \infty & \textrm{if}\ x = 0 \\ 0 & \textrm{if}\ x \neq 0\end{cases}" alt="Dirac delta function."> -->

<div class="equation" align="center" data-raw-text="\delta = \begin{cases} \infty &amp; \textrm{if}\ x = 0 \\ 0 &amp; \textrm{if}\ x \neq 0\end{cases}" data-equation="eq:dirac_delta">
    <img src="https://cdn.rawgit.com/stdlib-js/stdlib/7e0a95722efd9c771b129597380c63dc6715508b/lib/node_modules/@stdlib/math/base/special/dirac-delta/docs/img/equation_dirac_delta.svg" alt="Dirac delta function.">
    <br>
</div>

<!-- </equation> -->

and is constrained to satisfy the identity

<!-- <equation class="equation" label="eq:dirac_delta_integral" align="center" raw="\int^{+\infty}_{-\infty} \delta(x)\ dx = 1" alt="Dirac delta function integral."> -->

<div class="equation" align="center" data-raw-text="\int^{+\infty}_{-\infty} \delta(x)\ dx = 1" data-equation="eq:dirac_delta_integral">
    <img src="https://cdn.rawgit.com/stdlib-js/stdlib/7e0a95722efd9c771b129597380c63dc6715508b/lib/node_modules/@stdlib/math/base/special/dirac-delta/docs/img/equation_dirac_delta_integral.svg" alt="Dirac delta function integral.">
    <br>
</div>

<!-- </equation> -->

Note that the [Dirac delta function][dirac-delta-function] is **not** a function in the traditional sense, as any real-valued function which is zero everywhere except at a single point, must have an integral equal to `0`.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-dirac-delta
```

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
var linspace = require( '@stdlib/array-linspace' );
var diracDelta = require( '@stdlib/math-base-special-dirac-delta' );

var x = linspace( -1.0, 1.0, 101 );
var i;

for ( i = 0; i < x.length; i++ ) {
    console.log( 'dirac(%d) = %d', x[ i ], diracDelta( x[ i ] ) );
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-dirac-delta.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-dirac-delta

[test-image]: https://github.com/stdlib-js/math-base-special-dirac-delta/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/math-base-special-dirac-delta/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-dirac-delta/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-dirac-delta?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-dirac-delta
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-dirac-delta/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-dirac-delta/main/LICENSE

[dirac-delta-function]: https://en.wikipedia.org/wiki/Dirac_delta_function

</section>

<!-- /.links -->
