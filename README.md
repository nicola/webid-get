# webid-get

Get a webid in any linked data format for browsers and Node.js

## Install

```bash
$ npm install --save webid-get
```

## Usage

```javascript
var webidGet = require('webid-get')

var uri = 'http://www.w3.org/People/Berners-Lee/card#me'
webidGet(uri, function (err, webid) {
  // webid will be a jsonld object by default
})
webidGet(uri, 'text/turtle', function (err, webid) {
  // webid will be a string of text/turtle
})
```

## Command line

See [webid-get-cli](https://npm.im/webid-get-cli)

## License

MIT &copy; Nicola Greco 2015