# DAY 3

### We went over the lab requirements
- Have the kids draw the pictures for the items on the menu
- Do a random page that has meet the chefs, not a requirement. Kids can dress up as chefs
- removebackground.com 100% free helps remove backgrounds and create pngs.
## HTML Validation
## We created a new directory for second demo.

## Anchor tags
- Tells html where to go when you click it
````
    <a href="index.html"> Home </a>
    <a href="menu.html"> Menu </a>
    <a href="hiring.html"> Hiring </a>
````
### Useful to navigate to different pages on your website

# REMEMBER THESE!!
- DRY - Don't Repeat Yourself
- DONT 
- WET - Write Everything Twice

### Attributes



### We were able add a tag to snap to the bottom of the page. So octave or hashtag tells it to snap to that specific id. 
````
    <a href="#snapToBot"> Snap To Bot </a>
    <p id = "snapToBot" style="margin-top:1500px;"> SNAP TO THIS </p>
````

References another website

````
    <a href ="https://www.amazon.com" target="_blank"> Amazon </a>
````

# Moved to new directory. FormDemo.

````
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Form Demo</title>
</head>
<body>
````

- Forms: we need to know where info is going and what the info looks like and HOW it is going

- ONLY that which is in the form will be submitted
- input = user given data
- TYPE tells the input what html validation to use, gives it context on type of styling it can use
- id is not required, used to select it for various purposes
- REMEMBER!!  PUT BUTTONS INSIDE FORM
- Method is how you are receiving the information. Through URL(GET) or body (post)-->
````
<form action="" method="GET">

  <label> First Name:
    <input type="text" name="first_name" required>
  </label>
````
- the error message that occurs, by default comes from the browser

````
  <br>
  <label> Last Name:
    <input type="text" name="last_name" >
  </label>
  <br>
  <label> Password
````
- type password masks the input
````
    <input type="password" name="password"
            pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}"
           title="Must contain at least one  number and one uppercase and lowercase letter, and at least 8 or more characters">
  </label>
  <br>
  <label> Email    
  <input type="email" name="email"  required pattern="[a-z0-9._%+\-]+@[a-z0-9.\-]+\.[a-z]{2,}$">
  </label>
````

- email type has built in validation. Does it have an ampersand dot something
- we add the required attribute to make it required

- "br" is a line break, oncce we get to css we cannot use this anymore

````
  <br>
````

- radio buttons, best used for when there are multiple options but we want only one answer

````

  <label> Gender

    <input type="radio" name="gender" value="male"> Male
    <input type="radio" name="gender" value="female"> Female
    <input type="radio" name="gender" value="other"> Other
  </label>
````
- "name" identifier has to be the same for all inputs, if not it allows multiple to be filled.
- we add the value attribute to determine what is returned when selected

````
  <button type="submit">Submit</button>
</form>
</body>
</html>
````
- need to submit the data
- Has a specific type behavior based on type

### Normal information is GET REQUEST, sends through the URL

### POST REQUEST, sends through the body of the request.
- confidential information