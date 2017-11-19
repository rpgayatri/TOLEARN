# Babel 

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