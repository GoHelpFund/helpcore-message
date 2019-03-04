# helpcore-message

[![Build Status](https://img.shields.io/travis/gohelpfund/helpcore-message.svg?branch=master&style=flat-square)](https://travis-ci.org/gohelpfund/helpcore-message)
[![NPM Package](https://img.shields.io/npm/v/@gohelpfund/helpcore-message.svg?style=flat-square)](https://www.npmjs.org/package/@gohelpfund/helpcore-message)

> Message Verification and Signing for helpcore-lib

helpcore-message adds support for verifying and signing help messages in [Node.js](http://nodejs.org/) and web browsers.

See [the main helpcore-lib repo](https://github.com/gohelpfund/helpcore-lib) for more information.

## Install

```sh
npm install @gohelpfund/helpcore-message
```

To sign a message:

```javascript
var bitcore = require('@gohelpfund/helpcore-lib');
var Message = require('@gohelpfund/helpcore-message');

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

Feel free to dive in! [Open an issue](https://github.com/gohelpfund/helpcore-message/issues/new) or submit PRs.

Please see [CONTRIBUTING.md](https://github.com/gohelpfund/aden/blob/master/CONTRIBUTING.md) on the HelpCore repo for information about how to contribute.

## License

Code released under [the MIT license](LICENSE).
