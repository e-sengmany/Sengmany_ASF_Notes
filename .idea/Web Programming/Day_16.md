# Web Programming - Day 16

## Reinforce the Process
1) Create Parent directory
2) Create index.ts
3) "npm init -y" command
4) update package.json
5) npx tsc --init, creates a tsconfig.json
6) Add running instructions for the ts file in to the tsconfig
7) Create src folder nd put index.ts into it
8) install package (use npmjs.com)
9) import/utilize package/module

**If there are any issues with package use "npm i" to check installs** 

- We made a interface monster that we imported into our index.ts

```java
//monsterType.js
export interface Monster{
  firstName: string;
  lastName?: string; //? makes it optional.
  age: number;
  type: "Human"|"Blob"| "Undead";
  moreInfo: string;

}
export interface SuperMonster extends Monster{
    powerLevel: number;
}

export enum MonsterType{
    Human = "Human",
    Blob = "Blob",
    Undead = "undead"
}
//index.ts
import {Monster, SuperMonster} from "./models/monsterTypes"

const monster1: SuperMonster = {
  firstName: "Dracula",
  age: 1000,
  type: "Undead",
  moreInfo: "Drinks human blood",
  powerLevel: 10000
};

const monster2: Monster = {
  firstName: "Blobbo",
  age: 3,
  type: "Blob",
  moreInfo: "absprb everything in sight"
}

const monster3: Monster = {
  firstName: "Alice Smith",
  age: 28,
  type: "Human",
  moreInfo: "Monster Researcher"
}
console.log(monster1);
console.log(monster2);
console.log(monster3);
```

