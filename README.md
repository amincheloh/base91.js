Description
===========

base91.js is a base91 implementation in javascript that allows encoding/decoding of data to/from an ASCII representation that is more compact than base64.

More information about the base91 algorithm itself can be found [here](http://base91.sourceforge.net/).

If this module not working for you please consider use upstream [base91](https://github.com/mscdex/base91.js).

Requirements
============

* [node.js](http://nodejs.org/) -- v6.4.0 or newer


Installation
============

    npm install base91-prebuilt


Example
=======

```javascript
var base91 = require('base91-prebuilt');

console.log(base91.encode('node.js rules!'));
console.log(base91.decode(base91.encode('node.js rules!')).toString());

// outputs:
// lref5gTT$FQ;C90ohA
// node.js rules!
```


API
===

Functions
---------

* **encode**(< _mixed_ >data) - _string_ - Encodes `data` and returns the resulting base91 representation. `data` can be a string or an Array-like object (e.g. Buffer in node.js, Uint8Array or Array in browsers).

* **decode**(< _string_ >encodedData) - _mixed_ - Decodes `encodedData` and returns the result. For node.js, it will return a Buffer, otherwise it will return a Uint8Array if available, or a plain Array as a final fallback.
