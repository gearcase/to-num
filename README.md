# to-num

> Converts the given value to a number.


[![MIT License](https://img.shields.io/badge/license-MIT_License-green.svg?style=flat-square)](https://github.com/gearcase/to-num/blob/master/LICENSE)

[![build:?](https://img.shields.io/travis/gearcase/to-num/master.svg?style=flat-square)](https://travis-ci.org/gearcase/to-num)
[![coverage:?](https://img.shields.io/coveralls/gearcase/to-num/master.svg?style=flat-square)](https://coveralls.io/github/gearcase/to-num)


## Install

```
$ npm install --save to-num 
```


## Usage

> For more use-cases see the [tests](https://github.com/gearcase/to-num/blob/master/test/spec/index.js)

```js
var toNumber = require('to-num');

toNumber(1);                // => 1
toNumber();                 // => 0
toNumber(null);             // => 0
toNumber(Number.MAX_VALUE); // => Number.MAX_VALUE
toNumber(Infinity);         // => Infinity

// boolean
toNumber(true);  // => 1
toNumber(false); // => 0

// string
toNumber('1');      // => 1
toNumber('0');      // => 0
toNumber('-1');     // => -1
toNumber('1.1000'); // => 1.1 
toNumber('-1.100'); // => -1.1
toNumber('01');     // => 1
toNumber('0.10');   // => 0.1
toNumber('1a');     // => NaN
toNumber('a1');     // => NaN

// binary
toNumber('0b01'); // => 1
toNumber('0b10'); // => 2
toNumber('0b11'); // => 3
toNumber('0b02'); // => NaN

// octal
toNumber('0o01'); // => 1 
toNumber('0o07'); // => 7
toNumber('0o10'); // => 8
toNumber('0o08'); // => NaN

// hex
toNumber('0x01');  // => 1 
toNumber('0x0F');  // => 15 
toNumber('0x0G');  // => NaN
toNumber('-0x01'); // => NaN
toNumber('+0x01'); // => NaN

// object
toNumber(new Object(1));   // => 1
toNumber(new Number(1));   // => 1
toNumber(new Number(1.1)); // => 1.1
toNumber(function () {});  // => NaN 
toNumber(new Object());    // => NaN
```

## Related

- [to-integer](https://github.com/gearcase/to-integer) - Converts the given value to an integer.
- [to-length](https://github.com/gearcase/to-length) - Converts value to an integer suitable for use as the length of an array-like object.
- [to-str](https://github.com/gearcase/to-str) - Converts the given value to a string.
- [to-lower](https://github.com/gearcase/to-lower) - Converts string, as a whole, to lower case.
- [to-upper](https://github.com/gearcase/to-upper) - Converts string, as a whole, to upper case.
- [to-path](https://github.com/gearcase/to-path) - Converts value to a property path array. 
- [to-source-code](https://github.com/gearcase/to-source-code.git) - Converts function to its source code.


## Contributing

Pull requests and stars are highly welcome.

For bugs and feature requests, please [create an issue](https://github.com/gearcase/to-num/issues/new).
