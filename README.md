base64-js
=========

`base64-js` does basic base64 encoding/decoding in pure JS.

[![build status](https://secure.travis-ci.org/beatgammit/base64-js.png)](http://travis-ci.org/beatgammit/base64-js)

Many browsers already have base64 encoding/decoding functionality, but it is for text data, not all-purpose binary data.

Sometimes encoding/decoding binary data in the browser is useful, and that is what this module does.

## install

With [npm](https://npmjs.org) do:

`npm install base64-js` and `var base64js = require('base64-js')`

For use in web browsers do:

`<script src="base64js.min.js"></script>`

[Get supported base64-js with the Tidelift Subscription](https://tidelift.com/subscription/pkg/npm-base64-js?utm_source=npm-base64-js&utm_medium=referral&utm_campaign=readme)

## methods

`base64js` has three exposed functions, `byteLength`, `toByteArray` and `fromByteArray`, each requiring a single argument. `toByteArray` and `fromByteArray` also accept an optional `alphabet` argument (see `alphabets` property below).

* `byteLength` - Takes a base64 string and returns length of byte array
* `toByteArray` - Takes a base64 string and returns a byte array
* `fromByteArray` - Takes a byte array and returns a base64 string

## properties

Use the `alphabets` property to do base64 transcoding with arbitrary alphabets. The included [url](https://tools.ietf.org/html/rfc4648#section-5) alphabet is implemented internally using this interface. Example:
```
b64.alphabets.custom = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!?'
var a = b64.toByteArray('aa+/')
var b = b64.fromByteArray(a, 'custom')
console.log(b === 'aa!?') // true
```

## license

MIT
