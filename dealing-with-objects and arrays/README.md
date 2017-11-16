# Dealing With Objects / Spread and Rest Operators and Object Literals

## Spread Operator

### Basic Example

```javscript
let a = [...'Nischal']
// Output is ["N", "i", "s", "c", "h", "a", "l"];
```

## Lets evolve the above example

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

/// We could simply do

const d =[..c]; // replace d=c with this pice of code

```

## More examples

```javascript

const fruits = ['apple', 'mango', 'berry'];
const ingredients = {
  fruits: ['banana', 'apple']
}

const allFruit = [...fruits, ...ingredients.fruits];
console.log(allFruit);
//Output is ['apple', 'mango', 'berry', 'banana', 'apple'];

```

## Even More Examples 

```javascript
  const animals = [
    {name: 'Koala', hasTail: false},
    {name: 'kangaroo', hasTail: true},
    {name: 'croc' , hasTail: true},
    {name: 'pelican', hasTail: false}
  ];

  // lets say we only want 1,2, and 4th item in a new array

  const indexAnimal = animals.findIndex((animal)=> animal.name==='croc');
  const newAnimals = [...animals.slice(0,indexAnimal), ...animals.slice(indexAnimal+1)];
  console.log(newAnimals);
  // The new output is [{name: 'Koala', hasTail: false},{name: 'kangaroo', hasTail: true},{name: 'pelican', hasTail: false}
  ]

```


## Spreading into a function

```javascript

const names = ['Nischal', 'Gautam'];

function alertNames(first,last){
  alert(` hey there ${first} ${last}`);
}

alertNames(...names);   // spread operator will spread the array into 2 strings as a function input
```

## Rest Operator


### 1st use case => on functions

1. Rest opearator literally grabs rest of the remaining values


```javascript

function hello(name, ...otherAttributes){
  console.log(name, ...otherAttributes);
}

hello('Nischal', 'human', 'not an alien');
// Output 'Nischal', ['human','not an alien'];
```


### 2nd Use case => while destructuring

```javascript

const runner = ['Nischal', 12.3,45.4, 45.0];
const [name, ...runs] = runner // grabs the rest of the values 


```

## Object Literals 

### Example 1 

```javascript

const name1 = "hello1";
const name2 = "hello2";
const name3 = "hello3";

const names = {
  name1,
  name2,
  name3
}

```

### Example 2 

```javascript 
const names = {
  create(){

  },
  delete(){

  }
}

// it would be written like this without es6

const names = {
  create: function(){

  },
  delete: function(){

  }
}
```