# Promises

## Working with promises

```javascript

const postPromise = fetch('http:api.something.com');
// postPromise doesn't have the data yet, it contains a promise
postPromise
.then(data => return data.json())
.then(data => {console.log(data)} )
.catch((err)=> {
  console.log(err);
})
);

//when then is called and the promsie is succssuflly resolved the only we can get the data.
```


```javascript

```