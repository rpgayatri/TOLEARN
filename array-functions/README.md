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
### `Array.of()` takes as many arguments and turns them into array 

```javascript
  const numbers = Array.of(1,2,3,4);
  // numbers is now an array
```

## Note that `Array.find` and `Array.findIndex` are prototype methods
## `Array.find()`

```javascript
const posts = [{code: '123', gg: 345}, {code: 'rt4', gg: 34}];
console.log(posts.find(post=> post.code==='123'));
// output {code: '123, gg: 345}
```

## `Array.findIndex()`

```javascript
const posts = [{code: '123', gg: 345}, {code: 'rt4', gg: 34}];
console.log(posts.findIndex(post=> post.code==='123'));
//Output is 0 because code 123 is in index 0 of the array
```

### So whats the big deal with `index()` and  `indexOf()` ?

## You have to do this do acheive the same results using map
```javascript

const posts = [{code: '123', gg: 345}, {code: 'rt4', gg: 34}];
const post = posts.map(post=> {
  if(post.code==='123'){
    return post
  }
});
console.log(post);





```
