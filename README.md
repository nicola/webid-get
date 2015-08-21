# webid-get

Get a webid graph for the browsers and Node.js

- `sameAs`, `seeAlso`, `prefs` link following

## Install

```bash
$ npm install --save webid-get
```

## Usage

```javascript
var webidGet = require('webid-get')

var uri = 'http://www.w3.org/People/Berners-Lee/card#me'
webidGet(uri, function (err, graph) {
  // webid will be a `rdf-ext` graph
})

var rdf = rdf.createGraph()
webidGet(uri, graph, function (err) {
  // webid will be a `rdf-ext` graph
})
```

## License

MIT &copy; Nicola Greco 2015
