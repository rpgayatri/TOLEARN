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
class Dog  {
  constructor(name, breed){
    this.name = name; 
    this.breed = breed;
  }
  bark() {
    console.log("BARK BARK!!");
  }
    // this method is only available to class not an object and is not inherited.
  static info(){ 
    console.log("A dog is better than a cat");
  }

  // this is accessed as a property not as a method
  get description(){
    return `${this.name} is awesome`;
  }

  set nickname(val){
    this.nick = val.trim().toUpperCase();
  }

  get nickname(){
    return this.nick;
  }
}

const miley = new Dog('miley', 'labrador');
miley.bark();
miley.description // this is a property not a method.
miley.nickname = "yoyo"; // this is also a property not a method call.
console.log(miley.nickname)

```

