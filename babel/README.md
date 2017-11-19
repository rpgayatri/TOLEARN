# Babel , Ployfill

## Notes

1. babel plugins are the individual plugins for example: arrow functions. The individual features of es2015 are plugins.

2. babel presets are the collection of plugins for example: arrow functions , rest operator , spread, destructuring. The collection of those plugins are presets.


### Instead of wiriting a .babelrc file you can do this on `package.json` file.

```json 
"babel" : {
  presets: ['es2015'],
  plugins: ['transform-object-rest-spread']
}

```

### Run this script to transform a file into browser runnable javascript in `package.json`

```json 
"scripts" : {
  "babel" : "babel index.js --watch --out-file compiled-index.js"
}
```


## Polyfill

1. polyfill makes  new methods that are not supported by browsers available 

#### For browsers

`
ployfill.io
`

1. it makes new methods like Array.from() available to older browsers
2.  it dynamically makes new methods available instead of making all the methods available.
3. use `require 'babel-polyfill'` for using with webpack
