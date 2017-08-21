# Hoisting in Javascript



## Variables
```javascript
var a = 1;
console.log(a);
// Gives an output of 1
```


#### what if we console.log() before the variable is created ?

```javascript
console.log(a);
var a = 1 ;

// this gives an output of undefined
// why undefined ? not an error , the obvious question is why not error because it doesn't exists yet.
// Well in javascript variables that are defined are hoisted on top without a value
// javascript takes all the variable definitions and put them on first but without the value, they are initialized as undefined.

```


## Functions

```javascript
hello();

function hello () {
  console.log('Hello World!')
}

// the output of this program would be Hello World! because javascript puts function definitions on the top
// meaning functions are hoisted on the top

```
