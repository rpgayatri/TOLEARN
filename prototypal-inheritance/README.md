# Prototyoe inheritance and es6 class



## prototypal inheritance

```javascript

function Dog(name, breed){
  this.name = name;
  this.breed = breed;
  this.laugh = function (){
    console.log("HAHA");
  }
}

Dog.prototype.bark = function (){
  console.log(this.name);
}
const gimmi = new Dog('Gimmi', 'husky');
gimmi.bark();
gimmi.laugh();
// gimmi inherits from Dog class
```

## es6 class 

```javascript 

class Dog () {
  constructor(name, breed){
    this.name = name; 
    this.breed = breed;
  }

  bark() {
    console.log("BARK BARK!!");
  }
}

const miley = new Dog('miley', 'labrador');
miley.bark();

```

