---
title: Debug Challenge 1 - Output Errors
permalink: /challenges/debug/1
---

[← Back](/challenges/)

### Introduction

The first kinds of errors you are likely to come across are bugs in code that is trying to perform output. Here are a few things to keep in mind:

- Are all of your opening and closing strings and parentheses matched up?
- Are your identifiers written with the correct name?
- Did you use the right symbol when typing a statement?
- Does your syntax highlighting look a little funky?

#### Skills to Practice

- Read and interpret compiler errors
- Fix syntax errors


### Challenge Tasks
1. Open your code editor and create a new program title "*Debug Challenge 1 Output Errors*".
2. One at a time, read the syntax error when you run your program. Identify and fix the error.
3. In a seperate text file named *fixes.txt*, identify each issue and what you did to fix the error.

**Copy and paste** the following code into your file.

```js
console.log("Hey Buddy!")
console.log('My name is Anthony!')
console.log(How's it going???)

console,log("I saw a dog today.")
concole.log("Have you seen a dog? You probably haven't."
```

#### Sample Error Output

Note, there may be more errors than the sample errors below.

```shell
---FIRST ERROR---
/home/runner/Debug-Challenge-1/index.js:1
console.log("Hey Buddy!"
            ^^^^^^^^^^^^

SyntaxError: missing ) after argument list


---SECOND ERROR---
/home/runner/Debug-Challenge-1/index.js:3
console.log(How's it going???)
            ^^^

SyntaxError: missing ) after argument list


---THIRD ERROR---
ReferenceError: log is not defined
    at /home/runner/Debug-Challenge-1/index.js:5:1


```

#### Sample Solution Output

```shell
Hey Buddy!
My name is Anthony!
How's it going???
I saw a dog today.
Have you seen a dog? You probably haven't.
```