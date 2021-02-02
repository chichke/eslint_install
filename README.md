# Installation

```
yarn add -D eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks husky lint-staged prettier

yarn add prop-types
``` 

# Add to package.json

 + ### Scripts :
```json
"scripts": {
...
"lint": "eslint .",
},
```
 + ### At the end :
```json
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.{js,ts,tsx}": [
      "eslint --quiet --fix"
    ]
  },
  "eslintIgnore": [
    "*-test.js"
  ],
  ```

Add both [.prettierrc]() and [.eslintrc.json]() to root of Project

# Useful resources

https://eslint.org/docs/user-guide/getting-started
https://github.com/typicode/husky#husky