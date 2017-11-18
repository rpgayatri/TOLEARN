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
## Creating your own promises

```javascript

const p = new Promise(resolve, reject => {
  setTimeout(()=> {
    reject(Error("Error happened here at this line"))
  }, 2000)
});

p
.then(data=> {
  console.log(data);
})
.catch(data=> {
  console.log(data);
})
```

## chanining promises



```javascript

const posts = [{id:1, title: "This is a post number 1", name: "Nischal"}];
const authors = [{id:1, name: "Nischal"}];
const desc = {yo: "dfdf", asd: "asdd"};


// promise to find a post by id
function findPostByid(id){
  return new Promise((resolve,reject)=> {
    const post = posts.find(post => post.id = id );
    if(post){
      resolve(post);
    }
    else{
      reject(Error("Post not found"));
    }
  });
}


// add mr to author details if the author name and author who posted the article are same;
function hydrate(post){
  return new Promise((resolve, reject)=> {
     const author =  authors.find(author=> author.name === post.name);
     &#1xF984;
     if(author){
       author.name = `Mr  ${author.name}`;
       resolve(author);
     }
    else {
      reject(Error("error on finding author"));
    }
     
  });
}


findPostByid(1)
.then(post=> {
  console.log(post);
  return hydrate(post)
})
.then(author=> {
  console.log(author);
});



             
    
      

      






```