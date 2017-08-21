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
