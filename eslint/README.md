# Eslint

1. Go ahead and make .eslintrc file on your home directory

```json
{
  "extends": "airbnb",
  "env" :{
    "browser": true, 
    "node": true,
    "jquery": true,
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
