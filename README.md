# lite-json-parse

Lightweight JSON parse errback function

Reduce the boilerplate of wrapping every JSON.parse in a try/catch block. This no frills nanolibrary will safely parse JSON and return a javascript object or an error object in a node-style error-first callback function.

Use in node or in the browser.

### Example
```javascript
var parseJSON = require('lite-json-parse');
var json = "{\"food\":\"pizza\",\"drinks\":[\"soda\",\"red pop\",\"root beer\"]}";

parseJSON(json, function (err, pizzaParty) {
  if (err) {
    // handle parse error object
    return console.log(err);
  }

  // success - have a pizza party!
  pizzaParty.drinks.forEach(function(beverage) {
    console.log(beverage);
  });
});
```

:floppy_disk:
