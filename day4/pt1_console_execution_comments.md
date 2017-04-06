# Console, execution order, comments

#### https://repl.it/languages/javascript <<< go here to run the code!

1. The console

Think of the console like a notepad. It will print whatever you tell it to.
```js
console.log(1+1)
// prints 2

console.log("hello")
// prints hello

```

It can print more than one thing if you separate it by commas.
```js

var word1 = "Hello"
var word2 = "Jennifer"
var number1 = 9

console.log(word1, word2, "number", number1)
// prints Hello Jennifer number 9

```

2. Comments

Inside the code, you can write notes to yourself using //
Every language has a different symbol for identifying comments 
```js
//This is a comment. This is not code and won't execute.
```

3. Execution Order

Javascript code executes from top to bottom.
```js
var number = 1

number + 1
number * 2
number / 2
number - 1

//******
//What does number equal now?
//******

```

4. Variable Declaration

Because of the execution order, you need to **declare** variables *before* you use them.
```js
console.log(sentence) // will return 'undefined'
var sentence = "I like ice cream."
console.log(sentence) // will return "I like ice cream."

```
