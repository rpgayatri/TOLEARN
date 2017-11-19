# Eslint

1. Go ahead and make .eslintrc file on your home directory

```json
{
  "extends": "airbnb",
  "env" :{
    "browser": true, 
    "node": true,
    "es6": true
  },
  "rules": {
    "no-unused-vars": 1,
    "no-console": 0,
    "import": 0,
    "func-names": 0,
    "react/prefer-es6-class": 0,
    "comma-dangle": 0
  }
}

```

1. 0 means disable
2. 1 means enable but it is a warning
3. 2 means enable

## But now you can easily use this by doing 

1. `npm install -g eslint`
1. `eslint --init`  and choose  setting that you need
1. Doing the above steps on your project directory will initialize eslint on your project.


# Some eslint hacks 

```javascript 
/*  globals  variable1 variable2 */
/* eslint disable */


``` 


## Notes

1. eslint plugins are the individual plugins for example: arrow functions. The individual features of es2015 are plugins.

2. Eslint presets are the collection of plugins for example: arrow functions , rest operator , spread, destructuring. The collection of those plugins are presets.