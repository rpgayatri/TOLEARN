# Prototyoe inheritance


```javascript

function Dog(name, breed){
  this.name = name;
  this.brreed = breed;
}

Dog.prototype.bark = function (){
  console.log(this.name);
}

const gimmi = new Dog('Gimmi', 'husky');
gimmi.bark();

```