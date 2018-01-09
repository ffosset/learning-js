# Learning JavaScript Basics

## Values
* ### String
  Sequence of characters, always between brackets </br>
  `"this is a phrase", "32", "flora"` <br>
  Concatenating strings: `"this is a phrase, 32, flora"`
  
* ### Number
  Never between brackets, can be floating or integer (without decimals) </br>
  `2, 43, 40192`
  
* ### Boolean
  Only has two values </br>
  `true, false`
  
* ### Null
  Is assigned nothing as a value </br>
  ```javascript
  var x = null;
  ```
  
* ### Undefined
  Is not assigned any value </br>
  ```javascript
  var x;
  ```

* ### NaN
  It means "Not a Number" and is returned indicating an error with number operations </br>
  `"hello"/5` <br>
   Returns `NaN`
   
* ### Falsy values
	- the Boolean value false
	- the null type
	- the undefined type
	- the number 0
	- the empty string `""`
	- the value NaN <br>
If the value is not in the list of falsly values, then it's truthy!

* ### Array
  Always between square brackets, can be heterogeneous (include different types of values), multi-dimensional (arrays inside arrays) and jagged (arrays with different values inside arrays) </br>
  
  *How to access one of the elements in the set?*
   ```javascript
    var list = ["Brussels", "Madrid", "Lisbon"];
    list[2];
   ```
   Returns `Lisbon`
  
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
  #### Custom Constructor
  Permits to set the properties for an object right when it is created. </br>
    ```javascript
	function Person(name,age) {
		this.name = name;
  		this.age = age;
	}
	var bob = new Person("Bob Smith", 30);
	var susan = new Person("Susan Jordan", 25);
   ```
   Properties are like variables that belong to an object, and are used to hold pieces of information. Properties can be accessed in two ways: </br>
  **Dot notation** with `ObjectName.PropertyName` </br>
  **Bracket notation** with `ObjectName["PropertyName"]`
   
## Comparison operators
Sign | Meaning 
--- | ---
**===** | equal to (strict equality has to be the same type and value to return true)
**!==** | not equal to
**>** | greater than
**<** | less than
**>=** | greater or equal
**<=** | less or equal
**%** | modulus

## Ternary operator
A conditional statement can be replaced by a ternary operator to code faster. It works like this: conditional ? (if condition is true) : (if condition is false) <br>

    var isGoing = true;
    var color;
    if (isGoing) {
    color = "green";
    } else {
    color = "red";
    }
    
    // replaced by
    
    var isGoing = true;
    var color = isGoing ? "green" : "red";

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
 
## Truth tables
Used to represent the result of all the possible combinations of inputs in a logical expression. A represents the boolean value on the left-side of the expression and B represents the boolean value on the right-side of the expression.
<img width="260" alt="screen shot 2017-11-13 at 17 50 53" src="https://user-images.githubusercontent.com/22743273/32737792-514b1204-c89b-11e7-85f9-3f13810d5e07.png">

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
  If you find yourself repeating else if statements in your code, where each condition is based on the same value, then it might be time to use a switch statement. You can add a default case to a switch statement and it will be executed when none of the values match the value of the switch expression.
  
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
* ### arrays of objects with loop
    ```javascript
    function Person (name, age) {
    	this.name = name;
    	this.age = age;
    }
    var family = new Array(); 
    family[0] = new Person ("alice", 40);
    family[1] = new Person ("bob", 42);
    family[2] = new Person ("michelle", 8);
    family[3] = new Person ("timmy", 6);
    
    for (var i = 0; i < family.length; i++) {
    	console.log(family[i].name);
    }
   ```


## Methods

* ### prompt
  Opens a dialogue box. Call either *.toUpperCase()* or *.toLowerCase()* on your prompt to ensure that the input you get from the user is capitalized the way you expect.
   ```javascript
    prompt("How old are you?").toUpperCase();
   ```
  
* ### confirm
  Opens a confirmation box the user has to check. </br>
   ```javascript
    confirm("You are leaving this page");
   ```
  
* ### console.log
  Will print out the value inside the parenthesis in the console.
   ```javascript
    console.log(["Print this out");
   ```
   
* ### set
   ```javascript
      var bob = new Object();
      bob.age = 17;
      bob.setAge = function (newAge){
         bob.age = newAge;
      };

      bob.getYearOfBirth = function () {
        return 2014 - bob.age;
      };
      console.log(bob.getYearOfBirth());
   ```

* ### this
  </br>

  
* ### push
  Add elements to the end of an array. Also, the `push()` method returns the length of the array after an element has been added. </br>
  `myArray.push("addedElement");` </br>

* ### pop
  Remove elements from the end of an array. Also, the `pop()` returns the element that has been removed in case you need to use it. </br>
  `myArray.pop();` </br>
  
* ### ()splice
 Add and remove elements from anywhere within an array. The first argument represents the starting index from where you want to change the array, the second argument represents the numbers of elements you want to remove, and the remaining arguments represent the elements you want to add. </br>
  `donuts.splice(1, 1, "chocolate cruller", "creme de leche");` </br>
   
## Properties
* ### .length
  Calculates the length of a string. </br>
  `"I am Flora".length;` </br>
  Result: 10

* ### .substring
  Chop up a string into the number of characters needed. </br>
  `"January".substring(0,3);` </br>
  Result: Jan

* ### variable
  Gives a name to a certain value. Variable with global scope: defined outside of a function. Variable with local scope: defined in a function (won’t work outside of it)</br>
   ```javascript
      var myAge = 24;
      //The value can be changed if we write this later on in the code//
      myAge = 30;
   ```
   ```javascript
      var myCountry = “Belgium”;
      myCountry.length = 7
      myCountry.substring (0, 3)
      // Result: Bel //
   ```

* ### function
  Block of code designed to perform a particular task after being called or invoked. The main advantage of using functions is defining one code to use it many times. The definition of a function is **ended with a semicolon**. </br>
   ```javascript
      var multiply = function(x, y) {
        return x * y;
      }
      multiply(2, 3);
      // Result: 6 //
   ```
   ```javascript
      var foodDemand = function (food) {
	       console.log(“I want to eat” + “ “ + food)
       };
       foodDemand(“chocolate”);
       // result: I want to eat chocolate //
   ```
   ```javascript
      var orangeCost = function(cost) {
	      var val = cost * 5;
        console.log(val);
      };
      orangeCost(5);
       // result: 25 //
   ```

