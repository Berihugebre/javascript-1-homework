> begin [the debugging exercises](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging) and paste each of your solutions into this file.  This will allow you to use your FCC exercises as a study reference later on  
> [completed example](https://github.com/AlfiYusrina/hyf-javascript1/blob/master/week1/freecode_camp_solutions.MD)  (wrong exercises, correct markdown styling)
## 1.Use the JavaScript Console to Check the Value of a Variable
```js
let a = 5;
let b = 1;
a++;
// Add your code below this line
console.log(a);

let sumAB = a + b;
console.log(sumAB);
```
## 2. understanding the Differences between the freeCodeCamp and Browser Console
```js

```
## 3.Use typeof to Check the Type of a Variable
```js
let seven = 7;
let three = "3";
console.log(seven + three);
// Add your code below this line
console.log(typeof seven);
console.log(typeof three);
```
## 4. Catch Misspelled Variable and Function Names
```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);
```
## 5.  Catch Unclosed Parentheses, Brackets, Braces and Quotes
```js
let myArray = [1, 2, 3];
let arraySum = myArray.reduce((previous, current) =>  previous + current);
console.log(`Sum of array values is: ${arraySum}`);
```
## 6. Catch Mixed Usage of Single and Double Quotes
```js
let innerHtml = "<p>Click here to <a href='#Home'>return home</a></p>";
console.log(innerHtml);
```
## 7. Catch Use of Assignment Operator Instead of Equality Operator
```js
let x = 7;
let y = 9;
let result = "to come";

if(x == y) {
  result = "Equal!";
} else {
  result = "Not equal!";
}

console.log(result);
```
## 8. Catch Missing Open and Closing Parenthesis After a Function Call
```js
//example
function myFunction() {
  return "You rock!";
}
let varOne = myFunction; // set to equal a function
let varTwo = myFunction(); // set to equal the string "You rock!"
//excerscies
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine();
console.log(result);
```
## 9. Catch Arguments Passed in the Wrong Order When Calling a Function
```js
function raiseToPower(b, e) {
  return Math.pow(b, e);
}

let base = 2;
let exp = 3;
let power = raiseToPower(base, exp);
console.log(power);
```
## 10. Catch Off By One Errors When Using Indexing
```js
function countToFive() {
  let firstFive = "12345";
  let len = firstFive.length;
  // Fix the line below
  for (let i = 0; i < len; i++) {
  // Do not alter code below this line
    console.log(firstFive[i]);
  }
}

countToFive();
```
## 11. Use Caution When Reinitializing Variables Inside a Loop
```js
function zeroArray(m, n) {
  // Creates a 2-D array with m rows and n columns of zeroes
  let newArray = [];
  for (let i = 0; i < m; i++) {
    // Adds the m-th row into newArray
     let row = [];
    for (let j = 0; j < n; j++) {
      // Pushes n zeroes into the current row to create the columns
      row.push(0);
    }
    // Pushes the current row, which now has n zeroes in it, to the array
    newArray.push(row);
  }
  return newArray;
}

let matrix = zeroArray(3, 2);
console.log(matrix);
```
## 12. Prevent Infinite Loops with a Valid Terminal Condition
```js


