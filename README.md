Yeoman Generator
================
[![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependencies][dependencies-image]][dependencies-url]

This module is a [Yeoman](http://yeoman.io) generator for [Node.js](https://nodejs.org/) modules.


## Getting Started

To use the generator, ensure that you have installed Yeoman:

``` bash
$ npm install -g yo
```

For a general overview of Yeoman generators, see the [Getting Started Guide](http://yeoman.io/learning/).


## Installation

``` bash
$ npm install -g @kgryte/generator-node-module
```

## Usage 

Once installed, navigate to the directory in which you want to place generated files and run

``` bash
$ yo node-module
```

The generator will provide a series of prompts and will use your answers to tailor the module files, providing a scaffold upon which you can immediately build.


### Prompts

The prompts are as follows...


#### Module Name

The module name.

__Note__: that using the generator requires internet access, as module name availability is confirmed on NPM via [npm-name](https://github.com/sindresorhus/npm-name). 


#### Git

You have the option to initialize the module directory as a Git repository. The default option is `Y`. Typing `enter` or `y+enter` will confirm initialization and do the following:

``` bash
$ git init
$ git remote add origin https://github.com/<user_name>/<repo_name>.git
$ git add -A
$ git commit -m "[INIT]"
```

The initialization process stops short of pushing the commit to the remote repository.


#### Repository

If you elected to initialize a local Git repository, you must specify the corresponding remote repository __path__.

__Note__: a repository path __must__ include the `user`/`organization` name to which the repository belongs. For example,

```
my-org/new-module
```


#### Author

Enter the primary author's name; i.e., in all likelihood that will be your name.


#### Email

If you have chosen to initialize the directory as a Git repository, the default will be the email associated with your Github account. This email should be a correspondence address for those individuals wanting to contact you directly with their questions and comments.

If the Github email address is fine, just type `enter`.


#### License

Enter the license holder for this module. The default is your name, but this could be the organization for which you work (say, if they are helping sponsor development) or some other entity.

If the default option is fine, just type `enter`.


#### Description

Enter the module description.


### Scaffold

Once you have answered all prompts, you will have the following scaffold:

```
benchmark/
examples/
	- index.js
lib/
	- index.js
test/
	- test.js
.gitignore
.gitattributes
.npmignore
.travis.yml
.jshintrc
.jshintignore
.editorconfig
LICENSE
Makefile
package.json
README.md
TODO.md
```

#### Dotfiles

These are standard fare. If you notice that files are neither tracking in Git nor making their way onto NPM, consult `.gitignore` and `.npmignore`. The scaffold includes a `.travis.yml` file for continuous integration purposes. Visit [Travis-CI](https://travis-ci.org/) to setup running builds.


#### Makefile

The `Makefile` includes methods to run tests and generate notes. To see TODOs and FIXMEs,

``` bash
$ make notes
```


#### License

The default license is the [MIT license](http://opensource.org/licenses/MIT).


#### Package.json

The generator creates a scaffold `package.json`, using the repository path to generate the Github repository urls. You need to manually add `keywords` and any additional `dependencies`.


#### Documentation

The generator includes a `TODO.md` file. Use this file for general TODOs which are not tied to any particular file line.

The `README.md` is a scaffold. You should add to the usage and example code sections.


#### Lib

The main library file `lib/index.js` is stubbed. The file includes a dummy method (`foo`).


#### Test

The generator creates a skeleton test file. Aim for 100% test coverage.


#### Benchmark

The generator creates an empty directory for benchmarks. Should the module warrant benchmarks, include the benchmark files in this directory.


#### Examples

The `examples/index.js` file should be modified to showcase the module and should correspond to the example provided in the `README`.


#### Node Modules

The generator will automatically run `npm install` and install any node modules used by the scaffold. If you need any additional dependencies,

``` bash
$ npm install <module_name> --save
```

or development dependencies (either for testing or examples)

``` bash
$ npm install <module_name> --save-dev
```



## Notes

If you opted to initialize the module as a Git repository, you will need to manually push changes to Github.

``` bash
$ git push origin master
```

By default, the generator generates a [Travis-CI](https://travis-ci.org/) `*.yml` file for continuous integration and uses [Coveralls](https://coveralls.io/) for tracking code coverage over time.



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

Copyright &copy; 2015. Athan Reines.




[npm-image]: http://img.shields.io/npm/v/@kgryte/generator-node-module.svg
[npm-url]: https://npmjs.org/package/@kgryte/generator-node-module

[travis-image]: http://img.shields.io/travis/kgryte/generator-node-module/master.svg
[travis-url]: https://travis-ci.org/kgryte/generator-node-module

[coveralls-image]: https://img.shields.io/coveralls/kgryte/generator-node-module/master.svg
[coveralls-url]: https://coveralls.io/r/kgryte/generator-node-module?branch=master

[dependencies-image]: http://img.shields.io/david/kgryte/generator-node-module.svg
[dependencies-url]: https://david-dm.org/kgryte/generator-node-module

[dev-dependencies-image]: http://img.shields.io/david/dev/kgryte/generator-node-module.svg
[dev-dependencies-url]: https://david-dm.org/dev/kgryte/generator-node-module

[github-issues-image]: http://img.shields.io/github/issues/kgryte/generator-node-module.svg
[github-issues-url]: https://github.com/kgryte/generator-node-module/issues
