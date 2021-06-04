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

# Configurable Write-Only Accessor

> [Define][@stdlib/utils/define-property] a configurable **write-only** accessor.

<section class="installation">

## Installation

```bash
npm install @stdlib/utils-define-configurable-write-only-accessor
```

</section>

<section class="usage">

## Usage

<!-- eslint-disable id-length -->

```javascript
var setConfigurableWriteOnlyAccessor = require( '@stdlib/utils-define-configurable-write-only-accessor' );
```

#### setConfigurableWriteOnlyAccessor( obj, prop, setter )

[Defines][@stdlib/utils/define-property] a configurable **write-only** accessor.

<!-- eslint-disable id-length -->

```javascript
var obj = {};
var val = '';

function setter( v ) {
    val = v;
}

setConfigurableWriteOnlyAccessor( obj, 'foo', setter );

obj.foo = 'boop';

var bool = ( val === 'boop' );
// returns true
```

</section>

<!-- /.usage -->

<section class="notes">
    
## Notes

-   Configurable write-only accessors are **enumerable**.

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint-disable id-length -->

<!-- eslint no-undef: "error" -->

```javascript
var setConfigurableWriteOnlyAccessor = require( '@stdlib/utils-define-configurable-write-only-accessor' );

function Foo( secret ) {
    if ( !(this instanceof Foo) ) {
        return new Foo( secret );
    }
    setConfigurableWriteOnlyAccessor( this, 'secret', setter );
    return this;

    function setter( v ) {
        secret = v;
    }
}

var foo = new Foo( 'beep' );

foo.secret = 'boop';
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

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-define-configurable-write-only-accessor/main/LICENSE

[@stdlib/utils/define-property]: https://github.com/stdlib-js/utils-define-property

</section>

<!-- /.links -->
