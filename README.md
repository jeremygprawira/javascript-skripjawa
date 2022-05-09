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
