# awelog
Awesome logger for node

https://github.com/ivogabe/extLog

I like extlog a lot, as it provides a nice minimal logger i can configure within the source code: 

Then you can create instances
```
  ExtLog = require("extlog");
  var logHttp = new ExtLog("http", "cyan"); 
```

### ES6 Logging 
```
   logHttp.info("Hello World");
   logDB.debug("Logging a string:", "A string...");
   log.debug(title:string, obj:any)
```

#### Better instanciating
```
   var log = require("awelog")(name:string, color:string, level:string|number)
```

#### Better logging
```
   log.debug(...obj:any)
   debug = (args...)->
      title = typeof args?[0]
      if title is "string"
        title = args.splice 0
```

#### Better error handling with Proxy Object
```
   log.any -> defaultback on log.debug so it does not crash node
```
