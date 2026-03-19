# Web Programming - Day 15

### **Monday will be final project pitches**
## Reinforcing process
1) Create Parent directory
2) Create index.js
3) "npm init -y" command
4) install package (use npmjs.com)
5) import/utilize package/module

## TypeScript
- Difference between compiler and transpiler
  - Compiler: compiles code to machine code
  - Transpiler: compiles code to human readable code, so essentially notes we as programs can read
- We used "npm install -D typescript"
  - "-D" is for development dependencies, which means it will only be installed in development environment
- FOR TYPESCRIPT, we do not have to import or utilize it, it is automatically installed
### **REMEMBER TO USE FILE TYPE .TS for typscript files

**SHOULD CONSOLIDATE ALL NOTES INTO ONE MD FILE**
- JM used command npx tsc --init to create tsconfig.json file
  - This creates a tsconfig.json file that tells you every configerable thing you can do with typescript
-changed index.js to index.tx and put into a folder called src
- we used npx tsc in the console to compile our typescript files.
  - it created a linked file called "index.js"
  - Any things we run in the console will be run in the index.js file

**"-G" tag is for global dependencies, which means it will be installed in all environments**

**"npm i" command is for installing dependencies and is a good way to check if packages were installed correctly**

- different .ts files cannot invoke seperate functions unless we make that file accessible to the index.js file using "export".
  -So in the exporting file,

### We then used index.ts to establish variable, compile it into index.js, then print console log of variable
