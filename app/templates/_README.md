<%= title %>
===
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Dependencies][dependencies-image]][dependencies-url]

> <%= description %>


## Installation

``` bash
$ npm install <%= name %>
```

For use in the browser, use [browserify](https://github.com/substack/node-browserify).


## Usage

``` javascript
var foo = require( '<%= name %>' );
```

#### foo()

What does this function do?


## Examples

``` javascript
var foo = require( '<%= name %>' );
```

To run the example code from the top-level application directory,

``` bash
$ node ./examples/index.js
```


## Tests

### Unit

Unit tests use the [Mocha](http://mochajs.org/) test framework with [Chai](http://chaijs.com) assertions. To run the tests, execute the following command in the top-level application directory:

``` bash
$ make test
```

All new feature development should have corresponding unit tests to validate correct functionality.


### Test Coverage

This repository uses [Istanbul](https://github.com/gotwarlost/istanbul) as its code coverage tool. To generate a test coverage report, execute the following command in the top-level application directory:

``` bash
$ make test-cov
```

Istanbul creates a `./reports/coverage` directory. To access an HTML version of the report,

``` bash
$ make view-cov
```


---
## License

[MIT license](http://opensource.org/licenses/MIT). 


## Copyright

Copyright &copy; <%= year %>. <%= author %>.


[npm-image]: http://img.shields.io/npm/v/<%= name %>.svg
[npm-url]: https://npmjs.org/package/<%= name %>

[travis-image]: http://img.shields.io/travis/<%= repo %>/master.svg
[travis-url]: https://travis-ci.org/<%= repo %>

[coveralls-image]: https://img.shields.io/coveralls/<%= repo %>/master.svg
[coveralls-url]: https://coveralls.io/r/<%= repo %>?branch=master

[dependencies-image]: http://img.shields.io/david/<%= repo %>.svg
[dependencies-url]: https://david-dm.org/<%= repo %>

[dev-dependencies-image]: http://img.shields.io/david/dev/<%= repo %>.svg
[dev-dependencies-url]: https://david-dm.org/dev/<%= repo %>

[github-issues-image]: http://img.shields.io/github/issues/<%= repo %>.svg
[github-issues-url]: https://github.com/<%= repo %>/issues
