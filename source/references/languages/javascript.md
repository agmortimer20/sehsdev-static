---
title: JavaScript Syntax Reference
---

[← Back](/references/)

**Note**, this list is not exhaustive. For a complete reference to the JavaScript programming language, see the JavaScript documentation provided by the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript).

### Contents

#### JavaScript Programming Basics
1. [Output with console.log()](#Output-with-console-log)
2. [Primitive Types](#Primitive-Types)
3. [Comments](#Comments)
4. [Math](#Math)
5. [String Formatting](#String-Formatting)
6. [Variables](#Variables)
7. [Input](#Input)
8. [Constants](#Constants)
9. [Math Object](#Math-Object)
10. [Misc. Operators](#Misc-Operators)

#### Control Flow
1. [Boolean Logic](#Boolean-Logic)
2. [If Statements](#If-Statements)

<br>
<hr>

### Output with console.log()

`console.log()` is a function for sending information to the user in a console, or terminal. A function performs some type of task. In this case, `console.log()` performs *output*, which is information that is supplied to the user from the computer.

```js
console.log("Hey buddy!")
console.log(777)
console.log("I like turtles.")
```

<hr>

### Primitive Types
- String - Text data. Must be surrounded by either single quotes `'` or double quotes `"`.
- Number - Numerical data. Can be integers or decimals.
- Boolean - Logical *true* or *false*
- Undefined - If a variable has not been assigned a value, it is *undefined*.
- Null - The absence of a value.

Examples of numbers, strings, and Boolean values:
```js
50 45 -99 100.3 -777.11

"Anthony is a cool guy." 'Person' "Cabbage" 'Ford F-150' "99 bottles"

true false
```

<hr>

### Comments

Comments serve two major purposes: documenting your code and disabling code for testing purposes. There are two types of comments, single-line and multi-line comments. Documentation comments can start on their own line or at the end of a statement.

```js
// This is a single line comment.
console.log() // Output a blank line.

/*  This is
    a multi-line
*   comment.
```

<hr>

### Math

- Math operators:

    `+` **Addition**

    `-` **Subtraction**

    `*` **Multiplication**

    `/` **Division**

    `%` **Modulus** - Remainder divison

- You can use parentheses to control order of operations.

    `3 + 3 * 10` = 33

    `(3 + 3) * 10` = 60

<hr>

### String Formatting

String formatting allows a software developer to make strings that are customized to the program. The string can include math expressions, other strings, or really any arbitrary code expressions.

#### String Concatenation

Use the plus sign `+` with a string to combine the values to make a single string.

```js
// Hello, I am 30 years old.
"Hello, I am " + (15 * 2) + " years old."
```

#### String Templating

String templates use backticks ( \`\` ) instead of quotes, and code expressions are inserted anywhere in a string surrounded by the `${ }` symbol.

```js
// Same result as the concatenation example.
`Hello, I am ${15 * 2} years old.`
```

<hr>

### Variables

Variables are used to store data. The data can be manipulated and shown to the user (if necessary). Declare a variable with the `var` keyword, followed by the identifier, or name.

```js
var person
```

To store, or assign, a value to a variable, use the *asignment operator* `=`.

```js
var name = "Mortimer"
var age = 30
```

Variables can be manipulated and used in various expressions. You only need to use the `var` keyword when you first create the value.

```js
var name = "Mortimer"
var age = 30
var money = 5

console.log(name) // Output the value stored in name. In this case, "Anthony"
age * 12 // Multiply the value stored in age by 12. In this case, the answer is 360
money + 500 // Add money and 500 together. The answer is 505.
```

To assign a new value to a variable, simply assign it a new value. If you want to manipulate the value stored in the variable and save the new result, make sure to use the variable in the expression.

```js
money = 1000 // Overwrite the value 5 with the value 1000
console.log(money) // The value 5 is gone. The new value in money is 1000

// Add 5 to the value stored in age, which is 30. Save the new value, 35, to the age variable.
age = age + 5

money = money + 100 // Add 100 to the money value, and save the new answer (105)
```

It's common to use variables with string formatting.

```js
var name = "Anthony"
var account = 500

// Output "Hello, my name is Anthony"
console.log(`Hello, my name is ${name}`)

// Output "My balance is $550"
console.log(`My balance is $${account + 50}`)
```

<hr>

### Input

#### Browser Input

To get input from the user without an HTML form, use `prompt()`. The function returns user input as a string.

```js
var name = prompt("Enter your name")
```

![JavaScript Prompt Function](/assets/img/references/js-prompt-function.png)

#### Console Input with Node.js

Node.js wasn't made for traditional console based applications. It's meant to be fast and efficient. You'll notice that input function pause the program, and Node.js was not made to pause. So, there isn't a built-in function for input. Luckily, Node.js has a huge ecosystem of third-party packages. For simple console input, use the npm package **readline-sync**.

Readline-sync has a function called `question()` that allows the user to enter input to the console. The function returns user input as a string.

*Install from the command line or the Repl package manager.*
```bash
npm install readline-sync
```

```js
// Node style require. Import readline sync
var readline = require("readline-sync")

var name = readline.question("Enter your name: ")
```

<hr>

### Constants

Constants are similar to variables in that they store values for use throughout a program. However, the value stored in a constant *cannot change* after it has been initialized. Use constants when you have a variable whose value should not change once it is initialized. The convention for naming a constant is to capitalize the entire identifier name.

```js
const TAX = 0.08

var subtotal = 10
var total = subtotal * tax

// This line would break the program because it's a constant.
// TAX = 0.09
```

If the last line that's commented out were to execute, this syntax error would appear.

```bash
Uncaught TypeError: Assignment to constant variable.
```

<hr>

### Math Object

JavaScript provides a number of useful functions and properties for performing math operations. For an exhaustive list, see the [MDN reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

`Math.PI` - Ratio of the a circle's circumference to its diameter. ~3.14.....
```js
2 * Math.PI * radius
```

`Math.ceil(x)` - Returns a number rounded up to the nearest integer. i.e. Always round up.
```js
Math.ceil(5.15) // Round up to 6
```

`Math.floor(x)` - Returns a number rounded down to the nearest integer. i.e. Always round down.
```js
Math.floor(10.99) // Round down to 10
```

`Math.round(x)` - Returns a number rounded to the nearest integer.
```js
Math.round(5.5) // Roud up to 6
```

`Math.pow(base, exp)` - Returns a number to the exponent power.
```js
Math.pow(2, 10) // 2 to the power of 10, or, 1024.
```

`Math.sqrt(x)` - Returns the square root of a number.
```js
Math.sqrt(4)
```

#### Math.random()

`Math.random()` is used to generate a pseudo-random random between 0 and 0.999 repeated. To generate a random range of numbers, multiply `Math.random()` by a whole number and round the result down.

```js
Math.floor(Math.random() * 10) // Example: 3
Math.floor(Math.random() * 10) // Example: 8

// To generate a number from 1-x, add one at the end of the expression
Math.floor(Math.random() * 100 + 1) // Random number from 1 to 100
```

<hr>

### Misc. Operators

#### Incerement and Decrement Operators

The increment and decrement operators are shorthands for adding one or subtracting one to a number variable.

```js
var number1 = 10
var number2 = 25

number1++ // number1 = number1 - 1. number1 is now 11
number2-- // number2 = number2 - 1. number2 is now 24
```

#### Combined Assignment Operators

Combined assignment operators are shorthands for when you are manipulating a variable's value, and saving the new result.

- `+=` **Addition assignment operator** - Shorthand for adding a value to a variable.
- `-=` **Subtraction assignment operator** - Shorthand for subtracting a value to a variable.
- `*=` **Multiplication assignment operator** - Shorthand for multiplying a value to a variable.
- `/=` **Division assignment operator** - Shorthand for dividing a value to a variable.
- `%=` **Remainder assignment operator** - Shorthand for dividing and storing the remainder.

```js
var number = 100

number += 50 // number = number + 50. number is now 150
number -= 25 // number = number - 25. number is now 125
number *= 100 // number = number * 100. number is now 12500
number /= 10 // number = number / 10. number is now 1250
number %= 30 // number = number % 30. number is now 20
```

<hr>

### Boolean Logic

Boolean algebra, or Boolean logic, is the study of expressions where the result is one of two values, *true* or *false*.

A Boolean, or Bool for short, is a data type in JavaScript representing the literal values `true` and `false`. They are **not** strings.

**Boolean variables**

```js
var isWinner = true
var running = false

// 'Has the player won? true'
console.log(`Has the player won? ${isWinner}`)

// 'Is the task running? false'
console.log(`Is the task running? ${running}`)
```

#### Operators

`==` **Equal To** - Returns `true` if the values are equal to eachother.

`!=` **Not Equal To** - Returns `true` if the values are **not** equal to eachother.

`>` **Greater Than** - Returns `true` if the value on the left is greater than the value on the right.

`<` **Less Than** - Returns `true` if the value on the left is less than the value on the right.

`>=` **Greater Than or Equal To** - Returns `true` if the value on the left is greater than or equal to the value on the right.

`<=` **Less Than or Equal To** - Returns `true` if the value on the left is less than or equal to the value on the right.

`!` **Not** - Returns the opposite of the expression result. i.e. `!true` is `false`, and `!false` is `true`.

`&&` **And** - Compound operator. Returns `true` if the expressions on both sides return `true`.

`||` **Or** - Compound operator. Returns `true` if at least one expression on *either* side returns `true`. Less *strict* than the `&&` operator.

#### Truth Tables

Truth tables are used to show different combinations of Boolean expressions and their results. Think of it like a multiplication table, or some other arithmetic table.

|   **Equal To (`==`)** |   **Result**  |
| :-------------------- | ------------: |
|   `100 == 100`        |   true        |
|   `100 == 99`         |   false       |
|   `"abc" == "abc"`    |   true        |
|   `"ABC" == "abc" `   |   false       |
|   `true == true`      |   true        |
|   `true == false`     |   false       |

|   **Not Equal To (`!=`)** |   **Result**  |
| :------------------------ | ------------: |
|   `100 != 100`            |   false       |
|   `100 != 99`             |   true        |
|   `"abc" != "abc"`        |   false       |
|   `"ABC" != "abc" `       |   true        |
|   `true != true`          |   false       |
|   `true != false`         |   true        |

|   **Greater than/Less than (`>`,`<`)**    |   **Result**  |
| :---------------------------------------- | ------------: |
|   `100 > 100`                             |   false       |
|   `100 > 99`                              |   true        |
|   `0 < 100`                               |   true        |
|   `0 < -1`                                |   false       |

|   **Greater than or equal to/Less than or equal (`>=`,`<=`)** |   **Result**  |
| :------------------------------------------------------------ | ------------: |
|   `100 >= 100`                                                |   true        |
|   `100 <= 99`                                                 |   false       |

|   **Not (`!`)**   |   **Result**  |
| :---------------- | ------------: |
|   `!true`         |   false       |
|   `!false`        |   true        |
|   `!(100 > 100)`  |   true        |

|   **And (`&&`)**                          |   **Result**  |
| :-------------------------------------    | ------------: |
|   `100 == 100 && "anthony" == "anthony"`  |   true        |
|   `100 == 99 && "anthony" == "anthony"`   |   false       |
|   `"abc" == "abc" && "ABC" == "abc"`      |   false       |
|   `10 > 100 && 90 < 10`                   |   false       |

|   **Or (\|\|)**                           |   **Result**  |
| :-------------------------------------    | ------------: |
|   `100 == 100 \|\| "anthony" == "anthony"`  |   true        |
|   `100 == 99 \|\| "anthony" == "anthony"`   |   true        |
|   `"abc" == "abc" \|\| "ABC" == "abc"`      |   true        |
|   `10 > 100 \|\| 90 < 10`                   |   false       |

### If Statements

An if statement will execute a section of code, known as a **code block**, if a boolean expression, known as a **condition** has a *true* result. If the condition is *true*, the code block, which is surrounded by the curly braces, will execute. If the condition is *false*, the code block is skipped over, and does not execute.

**Example**

```js
var number = 100

if (number == 100) {
    console.log("Code inside a code block.")
    console.log("More code inside a code block...")
}
```

**Animation**

<!-- Begin Canvas Animation -->

<div id="animation_container" style="background-color:rgba(255, 255, 255, 1.00); width:640px; height:480px">
    <canvas id="canvas" width="640" height="480" style="position: absolute; display: block; background-color:rgba(255, 255, 255, 1.00);"></canvas>
    <div id="dom_overlay_container" style="pointer-events:none; overflow:hidden; width:640px; height:480px; position: absolute; left: 0px; top: 0px; display: block;">
    </div>
</div>

<script src="https://code.createjs.com/1.0.0/createjs.min.js"></script>
<script src="/assets/js/if-statement-animation.js"></script>
<script>
var canvas, stage, exportRoot, anim_container, dom_overlay_container, fnStartAnimation;
(function init() {
	canvas = document.getElementById("canvas");
	anim_container = document.getElementById("animation_container");
	dom_overlay_container = document.getElementById("dom_overlay_container");
	var comp=AdobeAn.getComposition("C756B9C09D06134D9B51CB30F8548AFC");
	var lib=comp.getLibrary();
	handleComplete({},comp);
})()
function handleComplete(evt,comp) {
	//This function is always called, irrespective of the content. You can use the variable "stage" after it is created in token create_stage.
	var lib=comp.getLibrary();
	var ss=comp.getSpriteSheet();
	exportRoot = new lib.IfStatementAnimation();
	stage = new lib.Stage(canvas);	
	//Registers the "tick" event listener.
	fnStartAnimation = function() {
		stage.addChild(exportRoot);
		createjs.Ticker.framerate = lib.properties.fps;
		createjs.Ticker.addEventListener("tick", stage);
	}	    
	//Code to support hidpi screens and responsive scaling.
	AdobeAn.makeResponsive(true,'width',false,1,[canvas,anim_container,dom_overlay_container]);	
	AdobeAn.compositionLoaded(lib.properties.id);
	fnStartAnimation();
}
</script>

<!-- End Canvas Animation -->

#### Else If and Else

We can *branch* if statements with to other kinds of statements, `else if` and `else`.

- `else if` must follow and if statement, and will only check it's condition if the preceding if statement condition resulted in `false`. You can chain as many else if statements as you want, but they *must* come after the initial if statement.
- `else` must be at the end of an if or else if statement. It does not require a condition, and will execute if any preceding if or else if statement coniditions result in `false`.

**Example**
```js
var number = 100

if (number > 100) {
    console.log("number is higher than 100")
}
else if (number == 100) {
    console.log("number is 100")
}
else {
    console.log("number is less than 100")
}
```