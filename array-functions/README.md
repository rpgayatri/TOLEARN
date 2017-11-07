# Array Functions 

## `Array.from()`


### `Array.from()` takes array-ish and turns them into a true array

# Example 

```javascript

  const a = document.querySelectorAll('p');
  // This gives us [p,p,p]
  // But they are not actual arrays they are NodeList
  // To convert them into array we do
  const b = Array.from(a);
  // this gives us [p,p,p]
  // Now we can use map functions since it is an array
  b.map(c => {console.log(c.textContent)});
  // YOu can also do this 
  const b = Array.from(a, (z)=> return z.textContent);
```
## `Array.of()`
### `Array.of` takes as many arguments and turns them into array 

```javascript
  const numbers = Array.of(1,2,3,4);
  // numbers is now an array
```