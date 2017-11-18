# WTF, is this ?

1. implicit binding
2. explicit binding
3. new binding
4. window binding


## implicit binding 

```javascript
var me = {
  name: 'Nischal',
  sayHello: function (){
    console.log("Hello "+ this.name);
  }
}

me.sayHello();
// to determine what is 'this' we need to go on the function invocation part 
// go to the left of sayHello() its me so 'this' is me. 
```

### Another example for implicit binding

```javascript
var Person = function (age){
  return {
    age: age,
    sayAge: function (){
      console.log(this.age);
    }
  }
}

var nischal = Person(21)
nischal.sayAge();



```

## Explicit binding covered on call-apply-bind under seperate readme



## new Binding

```javascript

const Animal = function (name, color){
  // if new is invoked javasceript creates this here.
  this.name = name;
  this.color = color;
}

const tiger = new Animal('tiger', 'orange');

// if new keyword is used , `this` is bound to the new object being created.

```




## window binding

```javascript

var hello = function (){
  console.log(this.hi);
}

hello(); // undefined
window.hi = "Hi there";
hello(); // Hi there
```
