# Prototyoe inheritance

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