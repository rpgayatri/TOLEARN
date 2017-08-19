 # ```var, let and const ```

1. var is function scoped
2. You can redefine a var
  1. var hello = 1;
  2. var hello = 2;
3. let is block scoped
4. Blocks => ``` if() { }; ```  here if is block
5. Variable defined inside a function will not leak outside of function.
6. ```Object.freeze(objectName) ``` makes an object immutable.
 ```
if(true){
      let a = 10;
      var b= 20;
  }

  console.log(a); // cannot be accessed here because variables defined with let is block scoped
  console.log(b); // can be accessed here because var is function scoped.
  ```


```
  let winner = true
  if (true){
    let winner = false
  }
 console.log(winner)  //> output is true because let is scoped inside the block and cannot be acessed outside of the block.

```
