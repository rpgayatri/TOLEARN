# Destructuring


## Destructuring Objects

```javascript
  const settings = {secret, url, port};
  const { secret, url, port } = settings; //New es6 syntax

  //before this you would do this
  const secret = settings.secret;
  const url = settings.url;

```


## Other examples of destructuring Objects

```javascript
  //extending an object
  props = {height: 100, color: 'red'};
  {height, color, width} = settings; // This is how we do it
  { height = 100, color: 'blue', width = 300} = settings // This is how we pass default values
  {height: h, color: c, width: w} = settings // Now you can access height using h color using c and width using w
  console.log(w) //gives you the value of width

  // Lets mix it up
  const {width :w = 300, height: h = 200 } // console.log(w) gives you 300

```


## Destructuring Arrays
