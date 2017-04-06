# Functions

#### https://repl.it/languages/javascript <<< go here to run the code!

Functions are things that take an input and returns an output. 
Something goes in, something comes out.

1. Example
```js
function myNewFunction(word) {
    console.log("Hello " + word)
}

myNewFunction("world!"))
// console logs "Hello world!"

myNewFunction("Sarah!"))
// console logs "Hello Sarah!"

myNewFunction(999)
// console logs "Hello 999"
```


2. Declaring functions
    - There are two ways to declare functions in Javascript
```js

function functionOne() {
    console.log("Hi")
}

var functionTwo = function() {
    console.log("Hello")
}

```

3. Executing functions
    
```js

function functionOne() {
    console.log("Hi")
}

var functionTwo = function() {
    console.log("Hello")
}

functionOne() // hi 

functionTwo() // hello

```

4. Scope
    - Variables declared inside a function only exist inside the function.
    - Variables declared outside a function *can* exist inside the function too if they aren't inside another function's *scope* (or { } brackets)
```js
var declaredOutside = "I'm outside"

function scopePractice() {
    var declaredInside = "I'm inside!"
    console.log(declaredOutside, declaredInside)
} 

scopePractice() // returns "I'm outside! I'm inside!"

console.log(declaredOutside) // returns "I'm outside!"

console.log(declaredInside) // returns an error
```

5. Arguments
    - Arguments are what the things you pass into a function are called
    - The name of the argument can be anything and it'll only exist inside the *scope* (or { } brackets) of the function.
```js
function oneArgument(word) {
    console.log("I like " + word) 
}

oneArgument("cheese.") // "I like cheese"

// #################

function twoArguments(word, number) {
    console.log("I want " + number + word)
}

twoArguments(" puppies", 7) // I want 7 puppies

console.log(word, number) // error, because word and number are out of the functions's scope.
```

6. Using "return"
    - Functions are useful because they transform things in predictable ways.
    - So far, all of these functions have only console logged things.
    - Now, let's practice using 'return'.

```js
var word = "Dog"

function makeYelling(string) {
    return string + "!!@$#!@!!!!!!11"
}

makeYelling(word) // returns "Dog!!@$#!@!!!!!!11"

console.log(makeYelling(word)) // logs "Dog!!@$#!@!!!!!!11"

```

One more:
```js

var word = "Cat"

function makeYelling(string) {
    return string + "!!@$#!@!!!!!!11"
}

function addZ(string) {
    return string + "zzzzzzzzzzzzz"
}

function loveThings(string) {
    return string + addZ(string) + makeYelling(string)
}

loveThings(word) // returns Catzzzzzzzzzzzzz!!@$#!@!!!!!!11

console.log(loveThings(word)) //logs Catzzzzzzzzzzzzz!!@$#!@!!!!!!11

```