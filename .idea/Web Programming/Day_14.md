# Web Programming - Day 14

## Final Project
- CRUD adherrance
  - Delete: remove data, soft delete
    - Logging is not required.

### Forms
- Text or password input
-  Radio/checkbox input
-  File upload or select dropdown with 3 items


### UI and UX
- Design and Responsiveness
- All buttons, links, and inputs should work - no dead ends
- Images must have alt tags


## Decomposition
- Algorithms
- Agorithms and Decomposition
  - The best way to solve a problem is to decompose it
  - How do we break down a problem to smaller parts?


** We moved to firstNodeDemo program in IntelliJ.

### npm init -y
- npm init -y
  - created package.json, which is similar to build.gradle
  - "main" = our entry point. In this case it is index.js, also known as driver file.
  - 

**This is what was created using above command**

````
{
  "name": "firstnodedemo", // name of project
  "version": "1.0.0",
  "description": "",
  "main": "index.js", //entry point
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "type": "commonjs"
}
````

**If we just do npm init, terminal will prompt us the value for each field.**

**Remember that this file is just a string**

### Package.json
- Blue print for our project

### Steps we did for this project
1) Create Parent directory
2) Create index.js
3) "npm init -y" command
4) install package (use npmjs.com)
5) import package

### we installed cat-me

**Package.json = recipe, Package.lock.json = ingredients**

**Ensure that we make our node_modules folder in our project directory.**