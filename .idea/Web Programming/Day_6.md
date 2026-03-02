# Day 6

## CSS
- Cascading Style Sheets
- csszengarden.com, static webpage with css. Talks though what the different css properties do. Shows the same HTML but styled diferently.
* Anyting you see in the body can be manipulated with css.
1. Inheritiance
2. Specificity

## Three options
1. Inline CSS
2. Internal CSS
3. External CSS (most common)
4. CDN (Content Delivery Network)
* Inline and internal CSS allows you to write your CSS code inside of your HTML file. 
* External CSS allows you to write your CSS code in a separate file and link it to your HTML file.
* CDN is a service that allows you to link to a file on a server that is not your own. What we used to expxort fonts like google awesome.

````
    <body style="background-color: green";>
    
      <h1>Hey guys, hows it going?</h1>
    
    </body>
    
````
- Example of inline CSS.

````

<style>
  body{
    background-color: blue;
  }
</style>

````
- Example of internal CSS.

## SPECIFICITY
1. Inline CSS
2. Internal CSS
3. External CSS

* The closer to the element the higher the specificity or priority,
* 147colors.com, shows all the browsser safe colors,
* We can use HEX codes to get different colors. ex: #FF0000. Gives us options of 16777215 colors.
* Another option is RGB, which gives us 255, ex: rgb(255,0,0). Also has 16777215 options.

* Intelli J has a color picker option located in the tab near the line number. 

## Selectors
- If we want to tie a style to a specific element, we can make use of tags, classes, and ids.
- WE USE HASTAGS TO REFERENCE IDS IN CSS

````
    div{
      border: 5px black ridge;
    }
    
    #secondDiv{
      background-color: red;
    }
````

- To reference a class, we use a period and the class name.

````
.oddNum{
  background-color: green;
}
````
## REMEMBER THAT A SPACE HAS A VALUE!!
- big difference in the below code due to a space.

````
/*#firstDiv.oddNum{*/
/*  font-weight: bolder;*/
/*}*/
/*!*find the element that has an id of firstDiv and a class of oddNum*!*/

#firstDiv .oddNum{
  font-weight: bolder;
}
/*Find an ancestor that has the class firstDiv and a chilid with the oddNum tag*/

#firstDiv, .oddNum{
  font-weight: bolder;
}
/*Comma makes it apply to an element that has firstDiv ID OR element with oddNum*/
````

## What do we do if we cannot use IDs or classes as selectors?
- we use the nth-child selector or nth-of-type selector.
- nth-child is used to select the nth child of a parent element.
- nth-of-type is used to select the nth child of a specific type.

## Fonts and Font Family

## Homework go to font awesome and get the google kit.
