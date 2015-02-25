# angular-tmdb
Angular API wrapper for TMDB.org

##Containing two major modules (tmdbMovie, tmdbTV)

### Using

Just include the module in your index.html like:
```html
<script src="anular-tmdb.min.js"></script>
```

Then import it into the module where you want to use it:
```javascript
var myApp = angular.module('myApp',['tmdb']);
```

in your controller, service, factory, etc. you can use the specific module which you need:
```javascript
myApp.controller('GreetingController', ['$scope', 'tmdbMovie', 'tmdbTV', function($scope, tmdbMovie, tmdbTV) {
  // Do your stuff here
}]);
```

### tmdbMovie

Before you can use the module, you have to setup it by calling the setup method.

you have to pass your TMDB.org API key and, if you want to use HTTPS, useSSL = true.

```javascript
tmdbMovie.setup(apiKey, useSSL);
```