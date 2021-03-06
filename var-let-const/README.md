 # ``` var, let and const ```

1. `var` is function scoped
2. You can redefine a var `var a = 1; var a = 2;`
3. `let` is block scoped
4. Blocks => `if() { };`  here if is block
5. Variable defined inside a function with let will not leak outside of function.
6. `Object.freeze(objectName)` makes an object immutable.

 ```javascript
if(true){
      let a = 10;
      var b = 20;
  }

  console.log(a); // cannot be accessed here because variables defined with let is block scoped
  console.log(b); // can be accessed here because var is function scoped.
  ```


```javascript
  let winner = true
  if (true){
    let winner = false
  }
 console.log(winner)  //> output is true because let is scoped inside the block and cannot be accessed outside of the block.
 // let inside the if statement is only available inside the if statement
```


```javascript
var winner = false;
if(true){
  var winner = true;
}

console.log(winner) // the output is true because the value of var is available outside the block.
```

```javascript

const a = 1;
const a = 2; // will throw up an error Identifier 'a' has already been declared
a = 4 // re assigning the value to a const also throws an error;

```


```javascript

const a = { b: 1, c:2 };
const a= {};  // object cannot be redefined because it is defined as a const

```

```javascript

const a = { b: 1, c:2 };
a.b = 3 ;  //this will work because property can be changed even if the object is defined as a const

```

```javascript
const  d =1;
d=3 // cannot be updated;

let r = 4;
r =5; //now updated to 5
```



```javascript
  var a = 1 //exposed to global scope on window objecct
  // to solve this problem IIFE is used
  window.a // will give you 1

```

```javascript
  (function(){
    var a =1 ; // now a is only exposed to this function scope
    window.a // will give you undefined here
  })();

  //to fix this problem we wrap the let statement inside a block
  { // this will do the trick
    let b = 1; // not exposed to global scope
    window.b // will give you undefined
  ]
  window.b // gives undefined

```


``` Some javascript Gotchas ```

```javascript
for (var i =0 ; i< 3; i++) {
   setTimeout(function(){
     console.log(i);
    },1000)
  }

  // In this function any logical output we would like to think is it prints 0 1 2
  // But the output given by javascript is it prints '3' 3 times
  // why is that so ?
  // because the function is run after one second and the value of i after 1 sec becomes 3.
  // Why not 2 but 3 ?
  // well because once it becomes 2 and again goes on top of the loop i++ makes it 3
  // loop doesn't run but the value of i becomes 3. because the value of i is scoped outside of the loop it goes till i ++.
  // if let is used the value of i cannot reach i++, because let is block scoped.
  // after the loop is finished the value of i doesn't leak to i++ if let is used.
  // if you just replace let with var the output should be 0 1 2

```
