# Iterating over objects


### Using for of loop for objects
```javascript 

const obj = {
  a: 1,
  b: 2,
  c: 3
};

for(const prop of Object.keys(obj)){
  value = obj[prop]
  console.log(prop, value);
  // Output is
  //a 1
  //b 2
  //c 3
}


```
### Using for in loop for objects
```javascript 

const obj = {
  a: 1,
  b: 2,
  c: 3
};

for(const prop in obj){
  value = obj[prop]
  console.log(prop, value);
  // Output is
  //a 1
  //b 2
  //c 3
}
```

### Note
1. The most important difference here is that `for in loop` only takes in the index and `for of ` takes the index and values but they both are able to loop over falsy arrays.

