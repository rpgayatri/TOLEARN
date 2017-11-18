# WTF, is this ?

1. implicit binding
2. explicit binding
3. new binding
4. window binding




## Explicit binding covered on call-apply-bind under seperate readme



## new Binding

```javascript

const Animal = function (name, color){
  // if new is invoked javasceript creates this here.
  this.name = name;
  this.color = color;
}

const tiger = new Animal('tiger', 'orange');

// if new keyword is used , `this` is bound to the new object being created.

```




## window binding 

```javascript
  

```