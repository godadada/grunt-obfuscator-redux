
# grunt-obfuscator-redux

  Obfuscate Node.js projects via Grunt. This project was forked from the now-dormant Stephen Mathieson's [grunt-obfuscator](https://github.com/stephenmathieson/grunt-obfuscator), with additional features like multiple targets.

  Credits to [@alaimo](https://github.com/alaimo), who served as the inspiration for this fork.

[![Build Status](https://travis-ci.org/paambaati/grunt-obfuscator-redux.png?branch=master)](https://travis-ci.org/paambaati/grunt-obfuscator-redux) [![npm version](https://badge.fury.io/js/grunt-obfuscator-redux.svg)](http://badge.fury.io/js/grunt-obfuscator-redux)


## Installation

    $ npm install grunt-obfuscator-redux --save-dev

## Basic Usage

```js
grunt.loadNpmTasks('grunt-obfuscator-redux');

grunt.initConfig({
  obfuscator: {
    app: {
      src: [
        'app.js',
        'lib/*.js',
        'routes/*.js'
      ],
      options: {
        entry: 'app.js',
        out: 'obfuscated.js',
        strings: true,
        root: __dirname
      }
    }
  }
});
```

## Advanced Usage - Multiple Targets

```js
grunt.loadNpmTasks('grunt-obfuscator-redux');

grunt.initConfig({
  obfuscator: {
    app1: {
      src: [
        'app1.js',
        'lib/*.js',
        'routes/*.js'
      ],
      options: {
        entry: 'app1.js',
        out: 'obfuscated1.js',
        strings: true,
        root: __dirname
      }
    },
    app2: {
      src: [
        'app2.js',
        'lib/*.js',
        'utils/*.js',
        'routes/*.js'
      ],
      options: {
        entry: 'app2.js',
        out: 'obfuscated2.js',
        strings: true,
        root: __dirname
      }
    }
  }
});
```

## Options

### `files`

  An array of files to be obfuscated.  This must include every `require()`-ed file in your project in no particular order.  Wildcards `e.g. "./src/**/*.js"` are accepted.  

### `entry`

  Your project's entry point, for example `app.js`.

### `out`

  File to output to, for example `obfuscated.js`.

### `strings`

  Boolean option for obfuscating simple strings.  Defaults to `false`. If set to `true`, note that `use strict` has to be removed, as this option encodes all strings to octal representations. I'd suggest using [grunt-remove-usestrict](https://github.com/HAKASHUN/grunt-remove-usestrict) to remove them during build-time.

### `root`

  The base directory.  Usually `__dirname` works just fine.

## License 

(The MIT License)

Copyright (c) 2015 Ganesh Prasannah &lt;g.prasannah@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
