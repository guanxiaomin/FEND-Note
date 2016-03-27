# JavaScript

### NaN (Not a number)

```javascript
typeof(NaN) // "number"
NaN === NaN // false
isNaN(NaN) // "true"
isNaN(undefined) // "true"

NaN === NaN;        // falseNumber.NaN === NaN; // falseisNaN(NaN);         // trueisNaN(Number.NaN);  // true
function valueIsNaN(v) { 
	return v !== v; 
	}valueIsNaN(1);          // falsevalueIsNaN(NaN);        // truevalueIsNaN(Number.NaN); // true

```
### Start a HTTP Server

```bash
$ python -m SimpleHTTPServer 8080
$ ngrok 8080 // make server accessable on Internet
```
### HTML tags
* ```<figure>``` and ```<figcaption>``` [MDN article](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)
* ```<sup>``` <sup>1</sup> The HTML Superscript Element
* ```<hr>``` horizontal rule
* ```<s>``` <s>strikethrough</s>
* ```<em>``` <em>italic</em>

### jQuery selector
```javascript
$(.class).eq(index); // find index
$(.class).attr('href'); // get attribute "href"
```

### Backbone.js & ajax
Use ```fetch()``` and ```sync()``` method

```javascript
// collection
 app.SearchResults = Backbone.Collection.extend({
    
    model: app.Result,

    initialize: function(options) {
      this.query = options.query;
    },

    url: function() {
      return myURL + this.query;
    },

    parse: function(response) {
      return response.hits;
    },
  });
  
// view
	app.results.on('sync', function(){
        this.render();
   }, this);
  app.results.fetch({
    success: function(collection, response) {},
    error: function() {console.log('error')}
  });
```

### Jasmine

* [Asynchronous Support](https://jasmine.github.io/2.4/introduction.html#section-Asynchronous_Support)
* [More about ```done()```](https://github.com/jasmine/jasmine/issues/988)