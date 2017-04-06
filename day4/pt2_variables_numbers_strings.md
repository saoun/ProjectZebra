# Variables & Numbers & Strings

#### Try to answer without code then run these questions in repl.it to see the answers!

#### https://repl.it/languages/javascript <<< go here to run the code!

1. Math
```js
var number1 = 10
var number2 = 5

// ******
// What does number1 + number2 = ?
// ******

console.log(number1+number2)

```

2. String Concatenation
```js
var string1 = "Hello"
var string2 = " World"

// ******
// What does string1 + string2 = ?
// ******

console.log(string1+string2)

```

3. Javascript Conversion(pt1)
```js
var number1 = 5
var string1 = "5"

// ******
// what does number1 + string1 = ?
// ******

console.log(number1+string1)

```

4. Javascript Conversion(pt2)
```js
var number1 = 10
var string1 = "Hello"

// ******
// what does number1 + string1 = ?
// ******

console.log(number1+string1)

```

5. Variable Reassignment
```js
var number1 = 10
var number2= 5

number1 = number2
number2 = number1 + number2

// ******
// What do number1 and number2 equal now?
// ******

console.log("number1 = " + number1, "number2 = " + number2)
```

6. Operations with math operators (pt1)
```js
var number1 = 2
var number2 = 2

// ******
//Just read over these
// ******

// Addition
// ******
number1 + number2 // = 4

console.log("Addition | " + (number1 + number2))

// Subtraction
// ******
number1 - number2 // = 0

console.log("Subtraction | " + (number1 - number2))

// Multiplication
// ******
number1 * number2 // = 4

console.log("Multiplication | " + (number1 * number2))

// Division
// ******
number1 / number2 // = 1

console.log("Division | " + (number1 / number2))

// Modulus (division remainder)
// ******
number1 % number2 // = 0

console.log("Modulus | " + (number1 % number2))

// Parenthesis 
// ******
number1 - (number2 * number2) // = -2

console.log("Parenthesis | " + (number1 | (number2 * number2)))

```

7. Operations with assignment operators (pt2)
```js
var number1 = 2
var number2 = 2

// ******
// Incrementing
// ++ adds 1
// ******

number1++

console.log("Incrementing | " + number1)

/////////////////////////////////////////////////////////

var number1 = 2
var number2 = 2

// ******
// Decrementing
// -- subtracts 1
// ******

number1--

console.log("Decrementing | " + number1)

/////////////////////////////////////////////////////////

var number1 = 2
var number2 = 2

// ******
// += makes the variable on the left EQUAL to itself + the other variable
// ******

number1 += number2

// ******
// What is number1?
// ******

console.log("Assignment Operators += | " + (number1))

/////////////////////////////////////////////////////////

var number1 = 2
var number2 = 2

// ******
// -= makes the variable on the left EQUAL to itself - the other variable
// ******

number1 -= number2

// ******
// What is number1?
// ******
console.log("Assignment Operators -= | " + (number1))

```


8. Difference between math operators and assignment operators?
```js

var number1 = 2
var number2 = 2

// ******
// number1 does not change in the line below - it stays as 2
// ******

number1 + number2 // equals 4
number1 + number2 // still equals 4
number1 // = 2

console.log("Number1 is still | " + number1)

// ******
// number1 DOES change in the line below - it becomes 4 then 6
// ******

number1 += number2 // number1 = equals 4
number1 += number2 // number1 = equals 6

console.log("Number1 is now | " + number1)

```

9. The += also works with strings!

```js
var string1 = "Little Bunny"
var string2 = " Foo"

string1 += string2
string1 += string2

// ******
// What does string1 equal now?
// ******

console.log(string1)

```

10. Construct a sentence!

```js
var numberOfCats = 0;
var sentence = ""

// ******
// Change the variables above to construct the sentence: "I have 3 cats!"
// Run this code in repl.it to see it
// ******

console.log(sentence)
```
