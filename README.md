# monacocoin Message Verification and Signing for Bitcore-monacocoin


[![NPM Package](https://img.shields.io/npm/v/bitcore-message-monacocoin.svg?style=flat-square)](https://www.npmjs.org/package/bitcore-message-monacocoin)
[![Build Status](https://img.shields.io/travis/monacocoinpay/bitcore-message-monacocoin.svg?branch=master&style=flat-square)](https://travis-ci.org/monacocoinpay/bitcore-message-monacocoin)
[![Coverage Status](https://img.shields.io/coveralls/bitpay/bitcore-message-monacocoin.svg?style=flat-square)](https://coveralls.io/r/monacocoinpay/bitcore-message-monacocoin?branch=master)

bitcore-message-monacocoin adds support for verifying and signing monacocoin messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main bitcore-monacocoin repo](https://github.com/monacocoinpay/bitcore-monacocoin) for more information.

## Getting Started

```sh
npm install bitcore-message-monacocoin
```

```sh
bower install bitcore-message-monacocoin
```

To sign a message:

```javascript
var bitcore = require('bitcore-lib-monacocoin');
var Message = require('bitcore-message-monacocoin');

var privateKey = bitcore.PrivateKey.fromWIF('cPBn5A4ikZvBTQ8D7NnvHZYCAxzDZ5Z2TSGW2LkyPiLxqYaJPBW4');
var signature = Message('hello, world').sign(privateKey);
```

To verify a message:

```javascript
var address = 'n1ZCYg9YXtB5XCZazLxSmPDa8iwJRZHhGx';
var signature = 'H/DIn8uA1scAuKLlCx+/9LnAcJtwQQ0PmcPrJUq90aboLv3fH5fFvY+vmbfOSFEtGarznYli6ShPr9RXwY9UrIY=';
var verified = Message('hello, world').verify(address, signature);
```

## Contributing

See [CONTRIBUTING.md](https://github.com/monacocoinpay/bitcore-monacocoin/blob/master/CONTRIBUTING.md) on the main bitcore-monacocoin repo for information about how to contribute.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc. Bitcore is a trademark maintained by BitPay, Inc.

