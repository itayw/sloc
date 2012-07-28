# sloc

## supported languages

- CoffeeScript
- JavaScript
- Python

## Usage

```
sudo npm install -g sloc
```

```
sloc <file>
```

Or use it in your own node module

```javascript
var fs    = require('fs');
var sloc  = require('sloc');

fs.readFile("mySourceFile.coffee", "utf8", function(err, code){

  if(err){ console.error(err); }
  else{
    stats = sloc(code,"coffeescript");
    console.log("total   lines: " + stats.loc);
    console.log("source  lines: " + stats.sloc);
    console.log("comment lines: " + stats.cloc);
  }

});
```

## Run tests

    npm test

## License

sloc is licensed under the GPLv3 licence