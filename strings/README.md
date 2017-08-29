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
