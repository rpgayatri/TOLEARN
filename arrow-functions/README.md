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

1. ```javascript
// if the function doesn't have any arguments there must be opening and closing brackets.
function hello (()=> {

})

```

2. ```javascript
  const name = () => { alert("hello world");}
  const name2 = (name) => {alert(`hello ${name}`);}
  name2();

```



#### Notes
1. You cannot use named functions with arrow functions.

```javascript
//You cannot do this
  hello () => { }  // You cannot do this.
 ```
