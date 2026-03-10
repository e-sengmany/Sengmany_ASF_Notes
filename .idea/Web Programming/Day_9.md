# Day 9

## JavaScript

### Arrays
- Went over an example of arrays that used the function filter() but it used the === operator. To test if it would return anything for === 'apple' but since there was not instance of just apple it would return nothing.
    - = means an assignment operator.
    - == means an loose equality operator.
      - just needs to have same value.
      - would be true because value matches
    - === means strict equality operator.
      - must have same data type and value
      - 5 === "5" would be false cause not a string

** Strings are just array of characters that are strung together.

### Useful String Methods
- .length
- .toUpperCase()
- .toLowerCase()
- .trim() = removes spaces from both ends of the string
- .slice() = can specify values in between an index range
  - words.slice(0, 7)
  - reminder, it is exclusive so it doesnt include values after the at request index values
- .split()
- .indexOf() = returns the index of the value of where requested value starts
  - if it is not found it returns -1, not 0 because it can be an index
- .substring() = returns a substring of the string
- .contains() = returns true or false if the string contains the value

## REMEMBER THAT SPACES/BLANKS HAVE VALUES!

## Arrays
- Append
  - push() = adds to the end of the array
  - unshift() = adds to the beginning of the array
- Remove
  - pop() = removes from the end of the array
  - shift() = removes from the beginning of the array

## Iterating and Iterators
### For Each
- forEach() = iterates through each element in the array and executes the function for each element.
### map()
- map() = iterates through each element in the array and executes the function for each element and returns a new array with the results.

### filter()
- filter() = iterates through each element in the array and executes the function for each element and returns a new array with the results.

## Functions
- Can be chained together
- use to show results or to return results

** Arguements vs Paramters
- Arguements are the values that are passed into the function
- Parameters are the variables that are defined in the function
- 
### Anonymous function
- function() {}
- not named
- immediately invoked function expression (IIFE)
### Fat arrow function
- () => {}
- pointer to location in the memory

````
function stuff(){
  console.log("stuff")
}
stuff()

function stuff2(age){
  return age + 10;
}

let result = stuff2(10)
console.log(result)

function stuff3(age, name, winner){
  return `${name} is ${age} years old and won${winner? "":"not"} the lottery!`
}

console.log(stuff3(20, "Jake", true))


let nameOfFunction = (name, age, winner) => {
  return `${name} is ${age} years old and won${winner? "":"not"} the lottery!`
}
console.log(nameOfFunction("Jake", 20, true))


//example of an anonymous function
// (function(){
//   console.log("I am a function")
// }())
//
// function doggy(){
//   return "woof"
// }
// doggy()
// let kittyCat = function(stuff, things){
//   return "meow"
// }
// kittyCat()

let squared = function(num) {
  return num * num
}
console.log(squared(5))

let square = (num) =>{
  return num*num
}
console.log(square(6))

let squares = num => num * num
console.log(squares(7))


let square4 = num => {
  num = num + num
  return num}

console.log(square4(8))

let canYouDrink = (age) => age >= 21 ? "Congrats!" : "No alcohol for you"
console.log(canYouDrink(21))
console.log(canYouDrink())

````
