# Day 8

## JavaScript
- It is a runtime language vs a compile language like java
  - We wont know if there are any errors until we run the code
  - Exists to work inside of the browser. 
- NODE JS, is just Javascript that runs outside of the browser.

** Important to know that some methods only exist in the browser.
- we can use the browsers devtools to practice javascript in the browser.
- We can also use the node js console to practice javascript. via command "node".

### JavScript
- When we run our javascript code, it runs in the console.
  - in  order to run the code in the console, use the command "node filename.js"
- If we attach HTML to our javascript code, it will run in the browser.
  - Has to be attaached in the body of the html file.
  - we use the following
  
```
  <script src="filename.js"></script>
```

- we opened the page but it didnt display anything becuase we didnt specify the content so it displaye in the broswer console.

** Javascript doesnt care if variables are identified with single or double quotes.

** we will use 'let' instead of 'var' or 'const'
  - Difference between 'let' and 'var' is that 'let' is block scoped.

### Javascript is asynchronous.
- Javascript is single threaded.
- Javascript is event driven.
- It doesnt run from top to bottom, although it starts there.
- Doest require semi colons, but it is good practice to use them.

## Precedence and Order of Operations
- Assignment starts right to left in javascript.
- It goes from right to left in javascript, starting with parenthesis

** You can open devtools on mac using CMD+OPT+I

** Everything that comes from prompts are strings. 
  - So when we get data from our forms it is in the form of a string. 

## Converting 
- Its called coercion in javascript

````
let answer = prompt("how old are you?");
answer = Number(answer)
console.log("you are " + answer + " years old");
console.log(typeof answer);
// will return age then type Number
````

** NaN = not a number. 
````
answer = parseInt(answer)
````
- will parse the string into a number. If the nnumber is in the back then will return NaN because it will identify the letter first and then signal NaN.

## Bolean types
- **falsey** values or values that are treated as false.
  - false, null, undefined, "" (because there is no space), 0
- **truthy** values
  - true, 1

## increment differences
````
count++ // post increment, same as count = count + 1
++count //pre increment, same as
count += count // same as count = count + count
````

- We covered addition symbol and concatenation cases with string.

## Template literals
- Must use a backtick
- allows us to use variables and expressions inside of the string.
- allows us to use multiline strings.

## Ternary operator
- if statement is a single line of code.
- ternary operator is a multi line of code.
````
age > 21 ? console.log("You are old enough to drink") : console.log("You are not old enough to drink")
````
- We can use ternary operator within different types of statements.
````
let sentence = `I love ${result} and I am ${age > 21 ? "old enough to drink": "not old enough to drink"}`
````

## Dates
````
const d = new Date()
console.log(d)
let day = d.getDate()
console.log(day)
let daysofWeek = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"]
console.log(daysofWeek[day])
console.log(`Today is ${daysofWeek[day]}`)
let hh = d.getHours()
let mm = d.getMinutes()
let ss = d.getSeconds()
console.log(hh + ":" + mm + ":" + ss)
// Another option
console.log(`The time is ${d.getHours()}:${d.getMinutes()}:${d.getSeconds()}`)
````
- We can use the date object to get the current date and time.
- Days are done from 0 to 6. with 0 being sunday.