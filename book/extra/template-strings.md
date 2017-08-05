# Template Strings


```javascript
function madLib() {
    var strings = arguments[0];
    var values = [].slice.call(arguments, 1);

    console.log('strings', strings);
    console.log('values', values);
}

var adjective = 'young';
var verb = 'ran';
var noun = 'store';

madLib`The ${adjective} man ${verb} all the way to the ${noun}`
```

https://github.com/denysdovhan/wtfjs#calling-functions-with-backticks