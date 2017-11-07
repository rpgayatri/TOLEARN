# Loops and arrays

## for of loop

```javascript 
  const games = ['football', 'table tennis', 'basketball'];

  for (const [i, game] of games.entries()){
    console.log(` ${game} is the ${i}+1 th item`);
  }
  // Games.entries gives acces to Array iterator 
  // [i,game]  is array destructuring
  // Go back to destructuring topic to see how arrays are   //destructured

```

## Getting all Arguments from a function 

```javascript 
  function helloWorld(){
    console.log(arguments); // logs 1,2,3 and other additional stuffs that you need to check it out yourself
  }

  helloWorld(1,2,3);
```


## Difference between for in loop and for of loop 

### For of loop 
```javascript 
  
  let a = [1,2,3,4];
  let total = 0 ;
  for( num of a) {
    total +=  num;
  }
  console.log(total) // Gives 10 as an output 
  
```

### for in loop

```javascript 
  let numbers = [1,2,3,4];
  let total = 0;
  for(num in numbers){
    total += num;
  }
  console.log(total);
  // Output is 00123 
  // because in loop gives the index of the array element not the element itself.

```

## Major takeaway:  the elements need not be true array to loop over it
### Example:

```javascript 
function sumNumbers() {
  let total = 0;
  for(arg of arguments){
    total += arg;
  }
  console.log(total);
  return total;
}

sumNumbers(1,2,3,4) // Return 10 
// THe arguments provided in sumNumbers functions are not array but are plain arguments but for of and for in loop still is able  to handle non true array elements.

// Takeaway: for in and of loop can handle non true arrays.
// Note: ForEach loop also can handle non non true array's.
```


### forEach Loop

```javascript 
  const numbers = [1,2,3];
  a.forEach((num)=>{ console.log(num)});
  // Downside of this loop 
  // 1. You cannot use break statement inside the looop if you need to stop the loop in the middle
  // 2. You cannot use continue statment inside the loop which is used for skipping an element while looping.

```

## Downside of for in loop
```javascript 

const a = [1,2,3];
for(b in a) {
  console.log(b);
}
``` 

1. THis loop also iterates over any other properties if a or any other methods or functions that might have been added to array prototype.

### See the example below 
```javscript 
Array.prototype.hello = function (){
  console.log(hello);
}
const numbers = [1,2,3,4];
  total = 0;
  for(num in numbers){
    console.log(num)
  }

  // The output of this program is 0,1,2,3 and hello 
```

### for of,  the best of the both worlds.

```javscript
  const numbers = [1,2,3];
  for( const num of numbers){
    console.log(num);
  }

  // THe output is what you expect it to be. 
  // try running the code in your browser console to see it for yourself

```
