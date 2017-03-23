# Learning JavaScript with Codeacademy

## Values
* ### String
  Sequence of characters, always between brackets </br>
  `"this is a phrase", "32", "flora"`
  
* ### Number
  Never between brackets, can be floating or integer </br>
  `2, 43, 40192`
  
* ### Boolean
  Only has two values </br>
  `true, false`

* ### Array
  Always between square brackets, can be heterogeneous (include different types of values), multi-dimensional (arrays inside arrays) and jagged (arrays with different values inside arrays) </br>
  
  *How to access one of the elements in the set?*
   ```javascript
    var list = ["Brussels", "Madrid", "Lisbon"];
    list[2];
   ```
   Result `Lisbon`
  
* ### Object
  Collection of information (**keys** and **values**) between curly braces
  #### Literal notation
    ```javascript
    var me = {
      name: value,
      age: value,
      nationality: value
    };
   ```
  #### Constructor
    ```javascript
    var me = new Object();
    me.name = "Flora";
    me.age = 24;
   ```


## Comparison operators
Sign | Meaning 
--- | ---
**===** | equal to
**!==** | not equal to
**>** | greater than
**<** | less than
**>=** | greater or equal
**<=** | less or equal
**%** | modulus


## Logical operators
* ### && (and)
  Evaluates to true if both expressions are true
    ```javascript
    var hungry = true;
    var foodHere = true;
    var eat = function() {
      if (hunger && foodHere) {
        return true;
      }
      else {
        return false;
      }
    };
   ```
* ### || (or)
  Evaluates to true when *one or the other or both* expressions are true
    ```javascript
    var tired = true;
    var bored = false;
    var nap = function() {
      if (tired || bored) {
        return true;
      }
      else {
        return false;
      }
    };
   ```
* ### ! (not)
  Makes true expressions false, and vice-versa
    ```javascript
    var programming = false;
    var happy = function() {
      if (!programming) {
        return true;
      }
      else {
        return false;
      }
    };
   ```
    `!true = false and !false = true`
 

## Conditional Statements
* ### if
  Used to specify a block of code that will be executed *if* a specified condition is true
    ```javascript
    if ("Flora".length < 7) {
      console.log("You have a short name!");
    }
   ```
* ### if / else
  Used to specify a block of code that will execute if the condition is false
    ```javascript
    if ("Flora".length < 7) {
      console.log("You have a short name!");
    }
    else {
      console.log("You have a long name!");
    }
   ```
* ### switch
  Used instead of the if / else if / else statement
    ```javascript
    var color = prompt("What's your favorite color?");
    switch(color) {
      case "red":
        console.log("Red is good!");
        break;
      case "blue":
        console.log("My favorite color too!");
        break;
      case "green":
        console.log("Green? What a weird choice!");
        break;
      default:
        console.log("I don't know that color");
     }
   ```


## Loops statements
Sign | Meaning 
--- | ---
**i++** | increment by 1
**i--** | decrement by 1
**i += x** | gincrement by x
**i -= x** | decrement by x

* ### for
  Used to execute a block of code a certain number of times
    ```javascript
    for (statement1, statement2, statement3) {
      code block to be executed
    }
    
    statement1 = where the loop starts
    statement2 = where the loop ends
    statement3 = by how much it loops
   ```
* ### while
  The loop will continue as long as the condition is evaluated true. It is useful when you don’t know how many times you will have to use the loop (ex: coin flipping)
    ```javascript
    var loopCondition = true;
    while (loopCondition) {
      console.log("Oops, try again!");
      loopCondition = false;
    }
   ```
* ### do/while
  Will execute the code block once, before checking if the condition is true, and then it will repeat the loop as long as the condition is true
    ```javascript
    var loopCondition = false;
    do {
      console.log("Loop at least once");
    }
    while(loopCondition);
   ```
* ### loops and arrays
    ```javascript
    var languages = ["HTML", "CSS", "Javascript", "Python", "Ruby"];
    for (i = 0; i < languages.length; i++) {
      console.log(languages[i]);
    }
   ```
* ### for/in


## Properties

## Methods
