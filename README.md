# Front-End Note
##Small Tips
### Start a HTTP Server

```
python -m SimpleHTTPServer 8888
```

### Backbone.js & ajax
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
