```javascript
var cdelta = require("cdelta");
var changed = cdelta();

var person = {
  name: "John"
};

console.log(changed(person)); // { name: "John" }
console.log(changed(person)); // { }
person.age = 32;
console.log(changed(person)); // { age: 23 }
person.age = 40;
person.name = "Jake";
console.log(changed(person)); // { name: "Jake", age: 40 }
```