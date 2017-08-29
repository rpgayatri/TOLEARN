# Strings

#### Before

```javascript
  let a = 1;
  console.log('this is number '+ a);
```

#### Now with template literals

```javascript
  //Fix above code with template literals
  //F
  let a = 1;
  console.log(`this is number ${a}`);
  // Results in More cleaner and simple code

```


#### create html markups with template literals



```javascript

const msg = {content: 'hello world'}
const code = ` <h1> ${msg.content} </h1>`
document.getElementById('content').innerHTML = code;

```


#### Tagged template literals
```javascript
  function trans(strings){
    return strings.toString().toLowerCase();
  }
  let content = trans`HELLO`;
  console.log(content);

  //Output will be hello

```


### String Methods

##### startsWith

```javascript
  const id = 'b1302912';
  const out = id.startsWith('b');
  console.log(out);
  // output is true

```

##### endsWith

```javascript
  const id = 'b1302912'
  const out  = id.endsWith('2');
  console.log(out);
  // Output is true

```


##### includes

```javascript
  const id = 'b1301010';
  const out = id.includes('3010');
  console.log(out);
  id.includes('B') // Output is false
  // Output true

```


#####  Repeat
```javascript
// Repeats a string Number of times
const 'hello'.repeat(100);

```
