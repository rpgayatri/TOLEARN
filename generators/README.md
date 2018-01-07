# Javascript Generators

 
 ```javascript 

const people = [{name: "Nischal", age: 25}, {name: "Ninu", age: 22}];

// written as function*
// can return multiple values
// can be invoked by using genName = gen();
// now call using genName.next()

function* loop(arr){
  for (var person of arr){
    yield person;
  }
}

const peopleGen = loop(people);

 ```

## Javascript generators with Ajax request 
 
 ```javascript

function ajax(url){
   fetch(url).then(data=> data.json()).then(data=> stepsGen.next(data))
 }
 
 function* steps(){
   console.log("Fetching Nischal");
   const nischal = yield ajax('https://api.github.com/users/ngprnk');
   console.log(nischal);
   console.log('Fetching fat Joe');
   const joe = yield ajax("https://api.discogs.com/artists/51988");
   console.log(joe);
 }


  const stepsGen = steps();

  stepsGen.next();


```