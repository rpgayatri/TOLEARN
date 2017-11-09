# Dealing With Objects 

## Spread Operator 

### Basic Example 

```javscript 
let a = [...'Nischal']
// Output is ["N", "i", "s", "c", "h", "a", "l"];
```

## lets evolve the above example 

```javascript 
const a = [1,2,3];
const b = [4,5,6];
const c = [...a, ...b, 7];
console.log(c);

// The output will be [1,2,3,4,5,6,7]
```

## Another useful usage

```javascript
const a = [1,2,3];
const b = [4,5,6];
const c = [...a, ...b, 7];
const d = c;
// if we change elemtnt of d
d[0] =10;
console.log(d);
// will give us [10, 2, 3, 4, 5, 6, 7 ]

console.log(c);
// if we console lof c this will also give us [10, 2, 3, 4, 5, 6, 7 ]

//many ways to fix this lets fix this by using spread operator

we could simply do 

const d =[..c]; // replace d=c with this pice of code 


```


