
Modules in a proper sense emerged in JavaScript with arrival of libraries like CommonJS and Asynchronous Module Definitions (AMD).

## CommonJS Modules

- `require()` and `module.exports`
- [[execution.synchronicity.async]] 

### Exporting 

```js
// myModule.js
function greet(name) {
    return `Hello, ${name}!`;
}

module.exports = greet;

```
For multiple exports
```js
// myModule.js
exports.greet = function(name) {
    return `Hello, ${name}!`;
};

exports.farewell = function(name) {
    return `Goodbye, ${name}!`;
};
```


### Importing

```js
// main.js
const greet = require('./myModule.js');
console.log(greet('Alice')); // Output: Hello, Alice!

// Or, if using multiple exports:
const myModule = require('./myModule.js');
console.log(myModule.greet('Alice')); // Output: Hello, Alice!
console.log(myModule.farewell('Alice')); // Output: Goodbye, Alice!


```


### Selectively loading modules

In [[lang.js.node]], you can load certain parts of modules selectively.

```js 
const { Buffer } = require('node:buffer');
```

## ES6 Modules

With arrival of [[lang.js.v.6]], modules were introduced natively in JS.

The existing `require` syntax was not used since `require` is asynchronous.

### Exporting

Named exports
```js
// utils.js
export const add = (x, y) => x + y;
export const multiply = (x, y) => x * y;
```

Default export

```js
// greeting.js
export default function greet(name) {
    return `Hello, ${name}!`;
}
```

### Importing

Named import 

```js
// main.js
import { add, multiply } from './utils.js';
console.log(add(2, 3)); // Output: 5
console.log(multiply(2, 3)); // Output: 6
```

Default import

```js
// main.js
import greet from './greeting.js';
console.log(greet('Alice')); // Output: Hello, Alice!
```

### Selectively loading

```js
// main.js
import { add } from './utils.js';
console.log(add(2, 3)); // Output: 5
```



## Es6 vs CommonJS

### [[execution.synchronicity]] and [[systems.char.performance.i.throughput]]

Loading is synchronous(step by step) for require on the other hand import can be asynchronous(without waiting for previous import) so it can perform a little better than require.

### Compatibility 

ES modules are compatible with Common JS modules. That is, you can import commonJS modules if you're using ES modules.

But you can't import ES modules if you're using CommonJS modules. A workaround is to use `import()` syntax.

Since the modules are not compatible you have to be careful while shipping your packages. 



#### Dual Package Hazard

Its a situation in which two versions of the same package get loaded within the same runtime environment. Of course, an application or package wouldn't do this intentionally, but it is common that the application itself loads one version, while a dependency of the application loads another version.


## Which module system?

### Default

Browsers didn't have module systems early on. Although, [[dev.tools.build.transformation.bundler]]s can process them. Even today, most modern browsers support only ES modules and have limited support for CommonJS modules.

[[lang.js.node]] treats all JS code as CommonJS modules.

Why though? => **Backward Compatibility** 

Many existing projects used commonJS modules, since it came first and  nodeJS also traditionally supported CommonJS. Keeping ES as default would mean rewriting or transpiling all that code. Keeping CommonJS as default maintains compatiblity with existing projects.

This allows the developers to gradually adopt the newer spec and stick with CommonJS until the benefits of migration outweigh the compatibility concerns. 


### Configuration

- **[[lang.js.org.packagejson]]**: `"type":"module"` indicates that the project uses ES modules.
- **File extensions** _(optional)_
    - `.cjs`: CommonJS module (Even in ES module project)
    - `.mjs`: ES Module (Differentiates ES modules from default `.js` CommonJS modules)

### Final Outcome of bundler

Even if you use an ES module system in your project, if your [[dev.tools.build.transformation.bundler]] emits commonJS code, then you are not really shipping an ES package.

### Interoperability

There are certain workarounds to ensure interoperability of both module systems in your project.

1. [[dev.tools.build.transformation.bundler]]: Bundlers can be configured to handle both modules. It takes care of dependencies and compatibility.
2. Use `import()` syntax to import ES modules in CommonJS modules. `import` statement works the same for ES and CommonJS modules in an ES module.


## References

- [import() - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/import)
- [Dual Package Hazard - GeoffreyBooth/dual-package-hazard - Github](https://github.com/GeoffreyBooth/dual-package-hazard): Example illustrating the hazard posed by dual CommonJS/ES module packages
- [JS Modules - GFG](https://www.w3schools.com/js/js_modules.asp)
- [Migrating from CommonJS - Pure ESM package](https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c)
- [Import vs Require - The Biggest JavaScript Divide - Matt Pocock - YouTube](https://youtu.be/6_JNPmjSevo?si=jpqZRov9HMwS7QM0)
- [The difference between "require(x)" and "import x"](https://stackoverflow.com/questions/46677752/the-difference-between-requirex-and-import-x)