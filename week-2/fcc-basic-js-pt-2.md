> complete the rest of [basic JS exercises](https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-javascript) on FCC and paste each of your solutions into this file.  This will allow you to use your FCC exercises as a study reference later on  
> [completed example](https://github.com/AlfiYusrina/hyf-javascript1/blob/master/week1/freecode_camp_solutions.MD) 

[Completed Excersise from 1 -78](https://github.com/Berihugebre/javascript-1-homework/blob/master/week-1/fcc-basic-js-pt-1.md) 
## 79. Counting Cards
```js 
var count = 0;

function cc(card) {
  // Only change code below this line
  switch(card){
    case 2:
    case 3:
    case 4:
    case 5:
    case 6:
    count = count + 1;
    break;
    case 7:
    case 8:
    case 9:
    count = count + 0;
    break;
    case 10:
    case 'J':
    case 'Q':
    case 'K':
    case 'A':
    count = count - 1;
    break;
  }
  if (count > 0){
    return count + ' Bet';
  }else 
  return count + " Hold";
  // Only change code above this line
}

// Add/remove calls to test your function.
// Note: Only the last will display
cc(2); cc(3); cc(7); cc('K'); cc('A');
```
## 80. Build JavaScript Objects 
```js
var myDog = {
  "name": "Boby",
  "legs": 4,
  "tails": 1,
  "friends": ["tom", "Jerry"] 
};
```
## 81. Accessing Object Properties with Dot Notation
```js
var testObj = {
  "hat": "ballcap",
  "shirt": "jersey",
  "shoes": "cleats"
};
var hatValue = testObj.hat;      // Change this line
var shirtValue = testObj.shirt; 
```
## 82. Accessing Object Properties with Bracket Notation
```js
var testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};
// Only change code below this line
var entreeValue = testObj['an entree'];   // Change this line
var drinkValue = testObj['the drink']; 
```
## 83. Accessing Object Properties with Variables
```js
var testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};
var playerNumber = 16;       // Change this Line
var player = testObj[playerNumber]; 
```
## 84. Updating Object Properties
```js
var myDog = {
  "name": "Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

// Only change code below this line.
myDog['name'] = 'Happy Coder';
```
## 85. Add New Properties to a JavaScript Object
```js
var myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

// Only change code below this line.
myDog.bark = 'woof';
```
## 86. Delete Properties from a JavaScript Object
```js
var myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};

// Only change code below this line.
delete myDog.tails;
````
## 87. Using Objects for Lookups
```js
function phoneticLookup(val) {
  var result = "";

  // Only change code below this line
  var lookup = {
    alpha: 'Adams',
    bravo: 'Boston',
    charlie : 'Chicago',
    delta: 'Denver',
    echo: 'Easy',
    foxtrot : 'Frank',
  };
  // Only change code above this line
  return result = lookup[val];
}
// Change this value to test
phoneticLookup("charlie");
````
## 88. Testing Objects for Properties
```js
var myObj = {
  gift: "pony",
  pet: "kitten",
  bed: "sleigh"
};

function checkObj(checkProp) {
  // Your Code Here
  if(myObj.hasOwnProperty(checkProp)){
    return myObj[checkProp];
  }else{
    return "Not Found";
  }  
}
// Test your code by modifying these values
checkObj("gift");
```
## 89. Manipulating Complex Objects
```js
var myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [ 
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  },
  // Add record here
   { "artist": "'Abrham Afewerki'",
    "title": "Singer",
    "release_year": 2006,
    "formats": [ 
      "CD",
      "DVD",
      "CD-ROM"
    ],
   }
];
```
## 90. Accessing Nested Objects
```js
var myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

var gloveBoxContents = myStorage.car.inside['glove box']; 
```
## 91. Accessing Nested Arrays
```js
var myPlants = [
  { 
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }  
];

// Only change code below this line

var secondTree = myPlants[1].list[1]; 
```
## 92. Record Collection
```js
// Setup
var collection = {
    "2548": {
      "album": "Slippery When Wet",
      "artist": "Bon Jovi",
      "tracks": [ 
        "Let It Rock", 
        "You Give Love a Bad Name" 
      ]
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette" 
      ]
    },
    "1245": {
      "artist": "Robert Palmer",
      "tracks": [ ]
    },
    "5439": {
      "album": "ABBA Gold"
    }
};
// Keep a copy of the collection for tests
var collectionCopy = JSON.parse(JSON.stringify(collection));

// Only change code below this line
function updateRecords(id, prop, value) {
if(!value){
  delete collection[id][prop];
  return collection;
}

if(prop !== "tracks" && value){
  collection[id][prop] = value;
}else{
  if( !collection[id].hasOwnProperty("tracks")) collection[id].tracks =[];
  collection[id].tracks.push(value);
}

  return collection;
}
// Alter values below to test your code
updateRecords(5439, "artist", "ABBA");
```
## 93.  Iterate with JavaScript While Loops
```js
var myArray = [];
// Only change code below this line.
var i = 0;
while( i <= 4 ){
  myArray.push(i);
  i ++;
}
```
## 94.  Iterate with JavaScript For Loops
```js
var myArray = [];

// Only change code below this line.
for(i = 1; i < 6; i ++ ){
    myArray.push(i);
}
```
## 95. Iterate Odd Numbers With a For Loop
```js
// Setup
var myArray = [];
// Only change code below this line.
for(var i = 1; i < 10; i += 2 ){
  myArray.push(i);
}
```
## 96. Count Backwards With a For Loop
```js
var myArray = [];

// Only change code below this line.
for (var i = 9; i > 0; i -=2){
  myArray.push(i);
}
```
## 97.  Iterate Through an Array with a For Loop
```js
var myArr = [ 2, 3, 4, 5, 6];

// Only change code below this line
var total = 0;
for (var i = 0; i < myArr.length; i++ ){
  total += myArr[i];
}
```
## 98. Nesting For Loops
```js
function multiplyAll(arr) {
  var product = 1;
  // Only change code below this line
  for (var i = 0; i < arr.length; i ++){
for (var j = 0 ; j < arr[i].length; j++){
  product = product * arr[i][j];
}
  }
 
  // Only change code above this line
  return product;
}
// Modify values below to test your code
multiplyAll([[1,2],[3,4],[5,6,7]]);
```
## 99. Iterate with JavaScript Do...While Loops
```js
do {
  myArray.push(i);
  i ++;
}while (i < 5);
```
## 100. Profile Lookup
```js
var contacts = [
    {
        "firstName": "Akira",
        "lastName": "Laine",
        "number": "0543236543",
        "likes": ["Pizza", "Coding", "Brownie Points"]
    },
    {
        "firstName": "Harry",
        "lastName": "Potter",
        "number": "0994372684",
        "likes": ["Hogwarts", "Magic", "Hagrid"]
    },
    {
        "firstName": "Sherlock",
        "lastName": "Holmes",
        "number": "0487345643",
        "likes": ["Intriguing Cases", "Violin"]
    },
    {
        "firstName": "Kristian",
        "lastName": "Vos",
        "number": "unknown",
        "likes": ["JavaScript", "Gaming", "Foxes"]
    }
];


function lookUpProfile(name, prop){
// Only change code below this line
for(let i = 0; i < contacts.length; i ++){
if(contacts[i].firstName === name){
    if (contacts[i].hasOwnProperty(prop)){
        return contacts[i][prop];
    }else {
        return "No such property";
    }
}
}
return 'No such contact'
// Only change code above this line
}

// Change these values to test your function
lookUpProfile("Akira", "likes");
```
## 101. Generate Random Fractions with JavaScript
```js
function randomFraction() {

  // Only change code below this line.
  return Math.random();
  // Only change code above this line.
}
```
## 102. Generate Random Whole Numbers with JavaScript
```js
var randomNumberBetween0and19 = Math.floor(Math.random() * 20);

function randomWholeNum() {
  // Only change code below this line.
  return Math.floor(Math.random()*10);
}
```
## 103. Generate Random Whole Numbers within a Range
```js
function randomRange(myMin, myMax) {
  return Math.floor(Math.random() * (myMax - myMin + 1)) + myMin; // Change this line
}
// Change these values to test your function
var myRandom = randomRange(5, 15);
```
## 104. Use the parseInt Function

The parseInt() function parses a string and returns an integer. Here's an example:

```js
function convertToInteger(str) {
  return parseInt(str);
}

convertToInteger("56");
```
## 105. Use the parseInt Function with a Radix

parseInt(string, radix);
And here's an example:
var a = parseInt("11", 2);
The radix variable says that "11" is in the binary system, or base 2. This example converts the string "11" to an integer 3.

```js
function convertToInteger(str) {
  return parseInt(str, 2 );
}

convertToInteger("10011");
```
## 106. Use the Conditional (Ternary) Operator

The conditional operator, also called the ternary operator, can be used as a one line if-else expression.
The syntax is:
```js
condition ? statement-if-true : statement-if-false;
```
```js
function checkEqual(a, b) {
 return a ===b ? true : false; 
}

checkEqual(1, 2);
```
## 107. Use Multiple Conditional (Ternary) Operators
```js
function checkSign(num) {
 return (num === 0)? "zero" : (num > 0)? "positive": "negative"
}

checkSign(10);
```


