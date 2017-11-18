# `call` , `apply` and `bind` Explicit Binding


## `call`

```javascript
// call allows you to explicitly determine the prosition of this
// IT defines the context of this 
// here weare calling displayname function and passing person as this

function displayName(){
  console.log("Hello", this.name);
}


var person = {
  name: "Nischal",
  age: 23
}

displayName.call(person);

```


## `apply`

```javascript
// apply does same thing as call but you can also pass second argument as an array.

function displayName(num1,num2,num3,num4){
  console.log("Hello", this.name, num1, num2, num3, num4);
}

num = [6,7,8,4];
var person = {
  name: "Nischal",
  age: 23
}

displayName.call(person, num);

```


## `bind`

```javascript

function displayName(){
  console.log("Hello", this.name, num1, num2, num3, num4);
}

num = [6,7,8,4];
var person = {
  name: "Nischal",
  age: 23
}

const newDisplayName = displayName.bind(person);

// bind method binds the to the object execpt that it returns a new function so that you can call it later at any point of time.


```
