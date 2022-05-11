# javascript-skripjawa
Definitely based on the freecodecamp.

## Comment
1. ``` // abc ``` - short comment, could be inline with the code, could also be in a stand-alone line.
   
   Example:
   ``` js
   var a = 1; // abc
   // def
   ```
3. ``` /* abc */ ``` - looooong comment, could be writing more than one line, must be in a stand-alone line.
   
   Example:
   ```js
   var a = 1;
   /*
   abcde
   fghij
   */
   ```
   
## Variables

### Data types
There are eight types of data that is in the JavaScript environment, which are:
| Data Types | Representation |
|------------|----------------|
| undefined | A variable that has not been assigned a value is of type ```undefined```.|
| null | no value |
| boolean | ```true``` or ```false``` |
| string | ```"123"```,```"abc"```|
| symbol | represent unique identifier |
| ```bigint``` | large integer number, can be helped with ```bigInt()``` or ending the number with -```n``` |
| number | ```123```, ```-1```, ```0,3``` |
| object | a collection of properties |

### Declaring Variables
```js
var myName;
```
Variable 101:
- should end the variable with semicolon ```;```
- the naming could be made up by numbers, letters, ```$```, or ```_```
- the naming could not have any space, or started with number
- the suggested naming rules would be with the ```camelCase``` system, in which:
  - **the first word** should start with **lowercase**
  - **the next word** and so on with **the uppercase.**
  - example: ```helloMyVariableIsCool```

### Storing values with the assignment operator
The key to assignment of a value to a variable is the ```=```.
```js
// If you have not declare the variable at first:
var a = 1;
// If you already declare the variable first:
var b; // the value of this variable (at first) is undefined.
b = 1;
```

### Assigning the value of one variable to another
The key is simple: ```=``` operator.
```js
var a;
a = 7;
var b;
b = a;
```

### ```let```
ES6 addition to declare a variable.

What makes ```let``` different than ```var``` is that, let can only be declared once.

Example:
```js
let abc = 1;
let abc = 2; // impossible el kontrolle

var def = 1;
var def = 2; // possible yet risky for large-lined code
```

### The almighty ```const```
```const``` is simply ```let``` but with a lock. It is impossible to change the value when you store the variable's value with the ```const``` keyword.

A note:

The naming of ```const```-based variable is different. ```const```-based variable will use the uppercase and ```_``` for the naming.

Example:
```js
const A_B = 1;
A_B = 2: // impossible
```

## Numbers
### Basic Operations
| Operations | Code | Result | 
|------------|------|--------|
| addition | ```const a = 10 + 5;``` | 15 |
| subtraction | ```const a = 10 - 5;```| 5 |
| multiplication | ```const a = 10 * 5;``` | 50 |
| division | ```const a = 10 / 5;``` | 2 |
| increment | ```let a = a + 1;``` is ```let a++;``` | **(EXPLANATION)** Sort of like "addition"? I guess? |
| decrement | ```let a = a - 1;``` is ```let a--;``` | **(EXPLANATION)** Sort of like "subtraction"? I guess? |

### Float

Float is more or less decimal. We could do operations such like multiplication with floats.
```js
const myDecimal = 4.2;
const mul = 2.0 * 2.5;
const quo = 4.4 / 2.0;
```
### Remainder

Remainder is literally remainder. Its the rest of the division that you did. We use ```%``` as the symbol for the remainder operation.
```js
const ha = 5 % 2;
// This is 1 because the rest of the division of 5 / 2 is 1.
```
### Compound Assignment with Augmented Operations

You basically simplify the addition of the variable. Let's say you have ```a = 5``` and ```a = a + 4``` you will definitely get 9 as the answer. In JavaScript this is not efficient yet. To simplify it:
```js
const a = 4;
a += 1;
// This brings 5
```
You can also do it with subtraction! AND LITERALLY OTHER OPERATIONS :)
```js
const b = 5;
b -= 4;
// This yield 1
```
## Strings 101
### Escape String Literal
This happens when we want to put quote marks on our string. To solve it, we can use ```\``` to avoid it. To use it:
```js
const a = "Jeremy said, \"abcdefh\".";
// Both backslashes should be infront of the quote marks.
```
### JS Single Quotes
The difference between double quotes and single qoute is none in JavaScript. But it is recommended, to use one type of quote when declaring string. This will affect the result aswell and also the use of ```<a>``` in which having so many characters and symbol in it. But you can still use two types of quotes as well.
```js
const goodStr = 'Jake asks Finn, "Hey, let\'s go on an adventure?"'; 
const badStr = 'Finn responds, "Let's go!"';
// Another example: Both OK!
const myStr = "<a href=\"http://www.example.com\" target=\"_blank\">Link</a>";
const myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```
### Escape String Literal: More
Escaping is very useful for:
- Help you to use character that feels impossible to use such as ```\r```
- Allow represent multiple quotes without the JavaScript misunderstand it,

Other escape:

| Code | Output |
|------|--------|
| ```\'``` | single quote |
| ```\"``` | double quote |
| ```\\``` | backslash |
| ```\n``` | new line |
| ```\r``` | carriage return |
| ```\t``` | tab |
| ```\b``` | word boundary |
| ```\f``` | form feed |

Example:

One variable for:
```
FirstLine
    \SecondLine
ThirdLine
```

Answer:
```js
const myStr = "FirstLine\n\t\\SecondLine\nThirdLine";
```

### String Concatenation
We could use ```+``` as the **concatenation** operator.
```js
const a = "abc " + "def.";
// Result: abc def.
// SPACES DEFINITELY MATTER HERE
```
We could also do it with ```+=``` as the conc. operator too.
```js
let a = "abc ";
a += "def.";
// Result: abc def.
```
So this concetenating style could be very useful like:
```js
const a = " abc ";
const b = "def " + a + " hij.";
// Result: def abc hij.
// SPACES DEFINITELY MATTER HERE
```


### Find the length of a string
using ```.length```
```js
// Setup
let lastNameLength = 0;
const lastName = "Lovelace";

lastNameLength = lastName.length;
```

### Bracket Notation in String
In string, bracket notation is meant to find the n character of the string exist.
```js
const a = "abc";
cons a1 = a[0];
// This will yield a
```
Notes: In programming everything always starts from 0.

To find the last notation:
```js
const a = "abc";
cons a1 = a[a.length - 1];
// This will yield c
```

### String Immutability
JavaScript string is immutable. This simply mean that, you cannot change one partially but you have to change everything.
```
let a = "abc";
a[0] = "d"; // This is impossible
a = "dbc"; // This is possible
```

## Array
```js
const a = [1, "abc"];
```

### Nested Array
This is basically **array inside an array**. This can be called as **multi-dimensional** array.

ps: I don't know things like this should go consistently. Like two attributes and next three, idrk.
```js
const a = [["a", 1], ["b", 3]]
```

### Block Notation: Array
Well this is to access certain array.
```js
const a = [1,2,3,4];
a[0]; // show 1
```

### Modifying Array
Oh great news, we could change parts of array not like in string where we should change the whole string in order to change a lil bit part of a string.
```js
const a = [2,3,4];
a[0] = 5; // a = 5,3,4
```
If we want to change a multi-dimensional array then we simply could at more bracket notation in the variable. So:
```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

arr[3]; // [[10,11,12], 13, 14]
arr[3][0]; // [10,11,12]
arr[3][0][1]; // 11
```

### Manipulate Array with ```.push()```
This is the way to add another data on the end of the array. With ```.push()``` you could add one or more data(s) to the end of array. If you add **more than one** data with ```.push()``` **and the ```[]``` notation**, then you will create a **nested array**.
```js
const a = [1,2];
a.push(3); // a = [1,2,3]

const b = [1,2];
b.push([4,5]); // b = [1,2,3,[4,5]]
```

### Manipulate Array with ```.unshift()```
```.unshift()``` is the way to add data on the ***first*** of array.
```js
const a = [1,2,3];
a.unshift(4);
// result of a = [4, 1, 2, 3]
```

### Manipulate Array with ```.pop()```
```.pop()``` is the way to remove data on the ****end**** of array.
```js
const a = [1,2,3];
const b = a.pop(); // 3
// result of a = [1, 2]
```
Don't worry, this is definitely working on any types of array, including multi-dimensional one.


### Manipulate Array with ```.shift()```
```.shift()``` is the way to remove data on the ***first*** of array.
```js
const a = [1,2,3];
const b = a.shift(); // 1
// result of a = [2, 3]
```

## Functions
```js
function functionName() {
   console.log("Hello World!");
}

functionName(); // To call the function
```

### Function: Passing Value
To pass value we could use **parameter**. Parameter acts as the placeholder for the value that will be input to the function.
```js
func functionName(a, b) {
   console.log(a, b);
}

functionName("a", "b");
```

### Function: Returning Value
We can pass values into a function with arguments. You can use a ```return``` statement to send a value back out of a function.
```js
func a(b) {
   return b + 3;
}

const c = a(5); // 8 -> You could assign it on a variable.
```
In short, you passed value of ```5``` to the function and returns the value of ```5 + 3```;

### Function: Global Scope and Functions
In JavaScript, ***scope*** refers to the visibility of variables. Variables which are defined outside of a function block have Global scope. This means, they can be seen everywhere in your JavaScript code.

Variables which are declared without the ```let``` or ```const``` keywords are automatically created in the global scope. This can create unintended consequences elsewhere in your code or when running a function again. You should always declare your variables with ```let``` or ```const```.

### Function: Local Scope
Local scope means, if you have variable inside the function then it only applies to that function only!
```js
function myTest() {
  const loc = "foo";
  console.log(loc);
}

myTest();
console.log(loc);
```

### Function: Undefined Value - SHOULD BE BACK
A function can include the ```return``` statement but it does not have to. In the case that the function doesn't have a ```return``` statement, when you call it, the function processes the inner code but the returned value is undefined.

Example
```js
let sum = 0;

function addSum(num) {
  sum = sum + num;
}

addSum(3);
```
```addSum``` is a function without a ```return``` statement. The function will change the global sum variable but the returned value of the function is **undefined**.

### Stand in Line - SHOULD BE BACK
In Computer Science a queue is an abstract Data Structure where items are kept in order. New items can be added at the back of the queue and old items are taken off from the front of the queue.

Example:
Write a function ```nextInLine``` which takes an array (```arr```) and a number (```item```) as arguments.

Add the number to the end of the array, then remove the first element of the array.

The ```nextInLine``` function should then return the element that was removed.

Solution:
```js
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  const removed = arr.shift();
  return removed;
  // Only change code above this line
}

// Setup
const testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));

/*
Result;
Before: [1,2,3,4,5]
1
After: [2,3,4,5,6]
*/
```

Explanation:
- Push item at the end of arr.
- Call the shift() method on arr to get the first item and store it in removed.
- Return removed.

Example Run:

- Test ```nextInLine([2,1]);``` runs.
- The ```nextInLine``` function is called. ```arr``` becomes ```[2]```. ```item``` becomes ```1```.
- ```arr.push(item);``` Pushes ```1``` to ```[2]```. So ```arr``` is now ```[2,1]```.
- ```const removed = arr.shift();``` removes the first element. So ```arr``` is now ```[1]```. ```2``` has been removed and is stored in ```removed```.
- ```return removed;```, ```2``` is returned.
- ***Note:*** You don’t actually need the variable ```removed```. The element ```removed``` can be returned directly using ```return arr.shift();```.

## Booleans, Operators, Conditionals
