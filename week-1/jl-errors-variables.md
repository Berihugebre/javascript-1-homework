> paste [this markdown](https://raw.githubusercontent.com/janke-learning/errors/master/functions.md) into this file and fix the errors!  
> [completed example](https://github.com/AlfiYusrina/hyf-javascript1/blob/master/week1/errors_solutions.MD) (of the old version)  
> references: [errors & life-cycle](https://github.com/janke-learning/errors-and-life-cycle), [exercise repo](https://github.com/janke-learning/errors)
# Function Errors

* [missing arguments](#missing-arguments)
* [is not a function](#is-not-a-function)

---

## missing arguments

broken code:
```js
function getNine {
  let x = 6;
  let y = 3;
  return x + y;
}
let result = getNine();
```
error message:
```
SyntaxError: missing ( before formal parameters
```
classification:
* creation phase
* syntax

the fix:
```js
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}
let result = getNine();
```
your notes:

[TOP](#function-errors)

---

## is not a function

broken code:
```js
let array = [];
array.length()
```
error message: 
```
TypeError: array.length is not a function
```
classification:
* creation phase
* semanitc

the fix:
```js
let array = [];
array.length;
```
your notes: length is not a function ,it is a type of array that returns numbers of elements in the array. 



[TOP](#function-errors)


___
___
### <a href="http://janke-learning.org" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/50098409-22575780-021c-11e9-99e1-962787adaded.png" width="40" height="40"></img> Janke Learning</a>
