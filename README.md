# Front-End Note
##Small Tips
### Start a HTTP Server

```
python -m SimpleHTTPServer 8888
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
