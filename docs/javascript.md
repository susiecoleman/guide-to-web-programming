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

### Operations on Numbers

In javascript it is possible to add `+` subtract `-` multiply `*` and divide `/` numbers. Numbers can also be incremented using `++` and decremented using `--`

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

## Loops

A common scenario in programming is to want to execute the same instruction multiple times. For example printing to the console. One solution is to write the same line of code multiple times:
```javascript
console.log("hello");
console.log("hello");
console.log("hello");
console.log("hello");
console.log("hello");
```

However this is time consuming (even with copy and paste) and if we wanted to print `goodbye` instead it would be neccessary to change it 5 times. A better solution is to use a loop.

### For Loops

A for loop will repeat until a condition is false. So if the condition is never false it will run forever.

```javascript
for(var i = 0; i < 5 ; i++) {
    console.log("hello");
}
```
[Interactive Example](https://jsbin.com/yuqetot/edit?js,console)

What the code above does is:

1. create a variable called `i` and give it the value `0`
2. check if `i` is less than `5`
3. execute the code inside the curly brackets: `console.log("hello")`
4. Add `1` to `i`

The code will continue to loop doing steps 2 to 4 until i is no longer less than 5. Once the loop has finished running the next line of code will be executed. For example for this program:

```javascript
for(var i = 0; i < 5 ; i++) {
    console.log("hello");
}
console.log("Finished executing loop");
```
[Interactive Version](https://jsbin.com/banaxek/edit?js,console)

The output would be:
```javascript
"hello"
"hello"
"hello"
"hello"
"hello"
"Finished executing loop"
```

The variable `i` we create can also be referred to in the code. For example if we wanted to print the numbers 1 to 10:

```javascript
for(var i = 1; i <= 10 ; i++) {
    console.log(i);
}
```
[Interactive Version](https://jsbin.com/wajamoh/edit?js,console)

#### For Loops and Lists

For loops can be used to iterate through lists.

```javascript
var fruits = ["apple", "banana", "cherry"];
for(var i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```
[Interactive Version](https://jsbin.com/nuboruf/edit?js,console)

In this example the condition that makes the loop stops looping is related to the length of the list. Also the variable `i` is used as the index to retreive items from the list.

# TODO Applying Javascript to HTML
