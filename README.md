# Node JS Global Object

Global Objects
- Class: Buffer
-  __dirname
-  __filename
-  clearImmediate(immediateObject)
-  clearInterval(intervalObject)
-  clearTimeout(timeoutObject)
-  console
-  exports
-  global
-  module
-  process
-  queueMicrotask(callback)
-  require()
-  setImmediate(callback[, ...args])
-  setInterval(callback, delay[, ...args])
-  setTimeout(callback, delay[, ...args])
-  TextDecoder
-  TextEncoder
-  URL
-  URLSearchParams
-  WebAssembly

### Global Objects
These objects are available in all modules. **The following variables may appear to be global but are not.** They exist only in the **scope of modules**.

-  __dirname
-  __filename
-  exports
-  module
-  require()

#### __dirname
```javascript
console.log(__filename);
// Prints: /Users/mjr/example.js
console.log(__dirname);
// Prints: /Users/mjr
```

#### __filename
```javascript
console.log(__filename);
// Prints: /Users/mjr/example.js
console.log(__dirname);
// Prints: /Users/mjr
```

#### exports
A reference to the module.exports that is shorter to type. See the section about the exports shortcut for details on when to use exports and when to use module.exports.

#### module
Reference: https://nodejs.org/api/modules.html#modules_the_module_object
In each module, the module free variable is a reference to the object representing the current module. For convenience, module.exports is also accessible via the exports module-global. module is not actually a global but rather local to each module.
- module.children
- module.exports
- module.filename
- module.id
- module.loaded
- module.parent
- module.paths
- module.require(id)

#### require()
Used to import modules, JSON, and local files. Modules can be imported from node_modules. Local modules and JSON files can be imported using a relative path (e.g. ./, ./foo, ./bar/baz, ../foo) that will be resolved against the directory named by __dirname (if defined) or the current working directory.
