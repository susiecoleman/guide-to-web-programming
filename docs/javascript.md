# Javascript

Javascript is a programming language and can be used to make a website interactive. It is used in front end web development but it is very versitile so it can also be used in back end development. The concepts covered are applicable to other programming languages.

Javascript is a series of instructions each instruction ends with a semicolon and the instructions are executed in the order they are written in the file.

## JSBin

[JSBin](https://jsbin.com/?js,console) is an online service that allows you to test out javascript. Javascript goes in the left hand pane then just click run to see the results. However to get anything to print out you will need to use `console.log()`. There are links to interactive examples of all the javascript code in this guide.

## Debugging - Console.log
The `console.log` command outputs a message to the [web console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console). This is useful for finding out what is going wrong with a program, for example logging the value of a variable.

```javascript
console.log("This is a console log.");
```
[Interactive Version](https://jsbin.com/lukeraz/edit?js,console)

## Variables

Variables are used to assign names to values. For example the number `200` could refer to anything but if it is assigned to a variable `var heightInCm = 200` it has a meaning. Variables can be reassigned to new values e.g.
```javascript
var heightInCm = 200;
heightInCm = 151;
```

In these examples `var` is used to create a variable. Javascript also has `const` and `let` for declaring variables but they work slightly differently. The [declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types) part of this guide covers the differences.

```javascript
var name;
name = "Susie";
var height = 171;

name = "Anna";
```
[Interactive Version](https://jsbin.com/fofajak/edit?js,console)

## Types

* Boolean - This type can have only 2 values `true` or `false`
* Number - These can be whole numbers (integers) or decimals (floating point numbers)
* Strings - A sequence of characters surrounded by quotes

```javascript
// Boolean values
var skyIsBlue = true;
var earthIsFlat = false;

// Integers
var total = 35;

// Floating point numbers
var pi = 3.14;

// Strings
var capitalCity = "London";
var meaningOfLife = "42";
var punctuation = "@£$`!!{}";
```
[Interactive Version](https://jsbin.com/ruqiros/edit?js,console)

### Comments
`//` In a javascript file denotes a comment. Any line that starts with `//` The browser will ignore. So in this example
```javascript
var x = 5;
// x = 6;
console.log(x);
```
The value printed out will be 5

## Arrays

An array is a list of items. For example
```javascript
[1,2,3];
[];
["apple", "banana", "cherry"];
[4, "cat", true];
```
are all arrays. But typically they are assigned to a variable

```javascript
var shoppingList = ["apple", "banana", "cherry"];
```

There are multiple operations that can be performed on an array. It is possible to get a specific item from an array by it's index:

```javascript
var shoppingList = ["apple", "banana", "cherry"];
var firstItem = shoppingList[0];
```

Note the index of an array start from zero. It is also possible to get the number of items in a list:

```javascript
var shoppingList = ["apple", "banana", "cherry"];
var length = shoppingList.length;
```

and add an item to the end of the list:

```javascript
var shoppingList = ["apple", "banana", "cherry"];
shoppingList.push("dates");
```
[Interactive version of all array examples](https://jsbin.com/fezetam/edit?js,console)

[Full guide on arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

## Conditional Statements

These are also know as `if else` statements. They are used to make sure that code is only executed if a statement is true. For example you might want your program to do something different depending on whether a variable has an even or an odd value. An if statement has the following structure:
```javascript
if(condition){
    statement;
} else {
    otherStatement;
}
```
where `statement` is executed if the condition is true and `otherStatement` is executed if it is false. 

### Conditions

The condition is a statement that evaluates to true or false. The expressions below all evaluate to true and show the different ways of comparing 2 items 
```javascript
// 3 is equal to 3
    3 === 3
// 3 is not equal to 2
    3 !== 2
// 3 is less than 5
    3 < 5
// 3 is greater than 1
    3 > 1
// 3 is less than or equal to 3
    3 <= 3
// 3 is greater than or equal to 3
    3 >= 3
```

### Putting it all together

```javascript
var number = 5;
if(number !== 5) {
    console.log("This is true");
} else {
    console.log("This is false");
}
```
[Interactive Version](https://jsbin.com/zotoqak/edit?js,console)

Conditional statements make code more interesting. Up to this point all the code has done the same thing every time it is run. With the introduction of if statement what the code does when executed now depends on whether or not the conditional statement is true or false. In the example above if number is assigned to 6 instead of 5 the code will do something different when it is run.

# TODO Incrementing numbers

# TODO For loops
A basic for loop
A for loop and an array

# TODO Applying Javascript to HTML
