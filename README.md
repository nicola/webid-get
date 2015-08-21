# webid-get

A WebID is URL that describes the identity of a user on the web. Getting WebID's data is as easy as a curl request

```bash
$ curl -X GET https://nicola.databox.me/profile/card#me
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .

<>
    <http://purl.org/dc/terms/title> "WebID profile of Nicola Greco" ;
    a <http://xmlns.com/foaf/0.1/PersonalProfileDocument> ;
    <http://xmlns.com/foaf/0.1/maker> <#me> ;
    <http://xmlns.com/foaf/0.1/primaryTopic> <#me> .
```

However, a WebID can point to other WebIDs of the same user (through `sameAs` and `seeAlso`), or to the user preferences and you very likely, you will need to follow these links to get the user data you want. This code could get very long and redundant, especially if you are using this in multiple projects. So, why not have a very simple command that does all of that for you?

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

var graph = rdf.createGraph()
webidGet(uri, graph, function (err) {
  // webid will be a `rdf-ext` graph
})
```

## License

MIT &copy; Nicola Greco 2015
