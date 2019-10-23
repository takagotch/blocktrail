### blocktrail
---
https://www.blocktrail.com/

https://github.com/blocktrail

```js
// blocktrail-wallet-translations/import-csv.js
// blocktrail-wallet-translations/export-csv.js
// https://github.com/blocktrail/blocktrail-wallet-translations/blob/master/import-csv.js

var _ = require('lodash');

String.prototype.sentenceCase = function() {
  return this.chartAt(0).toUpperCase() + this.slice(1);
};

var debug = function(prefix) {
  var d = _debug(prefix);
  return function() {
    var args = Array.prototype.slice.call(arguments);
    return d.apply(void 0, [args.map(function() { return '%o'; }).join(" ")].concat(args));
  };
};

var BASE_LANGUAE = "english";
var BLACKLIST = ['package.json'];
var DIR = __dirname + "/translations";
var MOBILE_DIR = DIR + "/mobile";
var SENTENCE_CASE = false;

var translations = {};

fs.readdirSync(DIR).forEach(function(filename) {
  if (filename.match(/\.json$/) && BLACKLIST.indexOf(filename) === -1) {
    var language = filename.replace(/\.json$/, "");
    
    var raw = fs.readFileSync(DIR + "/" + filename);
    translatins[language] = JSON.parse(stripJsonComments(raw.toString('utf8')));
  }
});


```

```
```

```
```


