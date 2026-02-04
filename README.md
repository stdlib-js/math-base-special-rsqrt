<!--

@license Apache-2.0

Copyright (c) 2019 The Stdlib Authors.

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

# Reciprocal Square Root

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the reciprocal of the principal [square root][square-root] of a double-precision floating-point number.

<section class="intro">

The reciprocal of the principal [square root][square-root] is defined as

<!-- <equation class="equation" label="eq:reciprocal_square_root" align="center" raw="\operatorname{rsqrt}(x)=\frac{1}{\sqrt{x}}" alt="Reciprocal square root"> -->

```math
\mathop{\mathrm{rsqrt}}(x)=\frac{1}{\sqrt{x}}
```

<!-- <div class="equation" align="center" data-raw-text="\operatorname{rsqrt}(x)=\frac{1}{\sqrt{x}}" data-equation="eq:reciprocal_square_root">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@5b8dab9d7f516fcc8e1741900ae1569e95470c73/lib/node_modules/@stdlib/math/base/special/rsqrt/docs/img/equation_reciprocal_square_root.svg" alt="Reciprocal square root">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import rsqrt from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-rsqrt@v0.2.3-deno/mod.js';
```

#### rsqrt( x )

Computes the reciprocal (inverse) square root of a double-precision floating-point number.

```javascript
var v = rsqrt( 1.0 );
// returns 1.0

v = rsqrt( 4.0 );
// returns 0.5

v = rsqrt( 100.0 );
// returns 0.1

v = rsqrt( 0.0 );
// returns Infinity

v = rsqrt( NaN );
// returns NaN

v = rsqrt( Infinity );
// returns 0.0
```

For negative numbers, the reciprocal square root is **not** defined.

```javascript
var v = rsqrt( -4.0 );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import discreteUniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-discrete-uniform@deno/mod.js';
import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@deno/mod.js';
import rsqrt from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-rsqrt@v0.2.3-deno/mod.js';

var opts = {
    'dtype': 'float64'
};
var x = discreteUniform( 100, 0, 100, opts );

logEachMap( 'rsqrt(%d) = %0.4f', x, rsqrt );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math-base/special/sqrt`][@stdlib/math/base/special/sqrt]</span><span class="delimiter">: </span><span class="description">compute the principal square root of a double-precision floating-point number.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-rsqrt.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-rsqrt

[test-image]: https://github.com/stdlib-js/math-base-special-rsqrt/actions/workflows/test.yml/badge.svg?branch=v0.2.3
[test-url]: https://github.com/stdlib-js/math-base-special-rsqrt/actions/workflows/test.yml?query=branch:v0.2.3

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-rsqrt/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-rsqrt?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-rsqrt.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-rsqrt/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-rsqrt/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-rsqrt/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-rsqrt/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-rsqrt/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-rsqrt/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-rsqrt/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-rsqrt/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-rsqrt/main/LICENSE

[square-root]: https://en.wikipedia.org/wiki/Square_root

<!-- <related-links> -->

[@stdlib/math/base/special/sqrt]: https://github.com/stdlib-js/math-base-special-sqrt/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
