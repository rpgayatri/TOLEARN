# Arrow Functions


```javascript

  function () {
  }

  // turn the above function into this
   () => {} // thats it. more simple and concise

```

## map and arrow function

```javascript
  dogs = ['huskey', 'spitz', 'bulldog'];

  const fancy = dogs.map( function( dog ) {
    return `fancy ${dog}`;
  });

  console.log(fancy);


  // Now lets convert this thing into arrow functions
  dogs = ['huskey', 'spitz', 'bulldog'];
  const fancy = dogs.map(( dog ) => {
    return `fancy ${dog}`;
  });
  console.log(fancy);

  //Same thing,  but more clean and readable code.
```

#### Other Examples
1.
```javascript
// if the function doesn't have any arguments there must be opening and closing brackets.
function hello (()=> {

})

```
2.
```javascript
  const name = () => { alert("hello world");}
  const name2 = (name) => {alert(`hello ${name}`);}
  name2();

```


### filter method

```javascript
  let ages = [40,50,60, 70, 20, 30 ,22];
  const old = ages.filter((age)=> { return age> 40 });
  console.log(old);

```



### Examples

```javascript
  // Filter
  persons = [{name: 'Nischal', age: 20}, {name: 'John', age: 19}]
  persons.filter((person)=> { return person.age===20});
```

```javascript
  // map
  persons = [{name: 'Nischal', age: 20}, {name: 'John', age: 19}];
b = persons.map((person) => { return person.age+1})
console.log(b);
//Output is 20 and 21
```

```javascript
// reduce

const a = [1,2,3];
let b = a.reduce((sum,num)=> {return sum+num },0)
console.log(b);

// Output is 6
```

#### Notes
1. You cannot use named functions with arrow functions.

```javascript
//You cannot do this
  hello () => { }  // You cannot do this.

 ```

 2. Arrow functions inherits the `this` from parent `this`

```javascript
 function () {
   console.log(this);

   function () {
     console.log(this);
   } // both `this` have different values
 }


 function () {
   console.log(this);

    () => {
     console.log(this);
   } // this this has the same value as upper `this`
 }
```


```javascript
// String interpolation
const number = 1;
const sentence = `inserting number ${1} inside this string`;
console.log(sentence);


```
