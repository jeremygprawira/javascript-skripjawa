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
### Operations
**Addition**
```js
const a = 10 + 5;
// value = 15
```
**Subtractionn**
```js
const a = 10 - 5;
// value = 5
```
**Multiplication**
```js
const a = 10 * 5;
// value = 50
```
**Division**
```js
const a = 10 / 5;
// value = 2
```
**Increment**
Sort of like "addition"? I guess?
```js
let a++;
```
is equal to:
```js
let a = a + 1;
```
**Decrement**
Sort of like "addition"? I guess?
```js
let a--;
```
is equal to:
```js
let a = a - 1;
```



