---
title: Algorithm - Generate Random Number
---

[← Back](/references/)

### Introduction

From generating sample data, to simulating uncertainty, generating random numbers can be very useful. Luckily, it's pretty simple to do.

### Language
1. [JavaScript](#JavaScript)
2. [C#](#c-sharp)

### JavaScript

JavaScript has a number of built-in math functions, one of which is called `Math.random()`. This function generates a random number between 0.0 and ~0.99999. Notice that it is never 1.0. The demo below breaks down the steps and then demonstrates the algorithm in one line.

```js
// One step at a time. Generate a random number between 0 and 9.

// Create random float.
var random1 = Math.random() // Example: 0.07437935702224197
var random2 = Math.random() // Example: 0.8166553542608308
var random3 = Math.random() // Example: 0.32402742725235156

// Multiply the float by a whole number get a random number in a given range.
random1 = random1 * 10 // 0.7437935702224197
random2 = random2 * 10 // 8.166553542608308
random3 = random3 * 10 // 3.2402742725235156

// Round the number down to get a clean integer.
random1 = Math.floor(random1) // 0
random2 = Math.floor(random2) // 8
random3 = Math.floor(random3) // 3


// All on one line.
Math.floor(Math.random() * 10)
Math.floor(Math.random() * 10)
```

If you want a random number that is in a range starting at 1, just add one at the end of the expression.

```js
// Generate a random number between 1 and 10
Math.floor(Math.random() * 10 + 1)

// Generate a random number between 1 and 50
Math.floor(Math.random() * 50 + 1)
```

<h3 id="c-sharp">C#</h3>

C# has a built-in class for generating random numbers named `Random`. A `Random` object contains a method called `Next()`, which has three variations, or *overloads*:

`Next()` - Returns a non-negative random integer

```cs
Random random = new Random();

random.Next(); // Example: 665004238
random.Next(); // Example: 392976750
random.Next(); // Example: 1178083184
```

`Next()` - Returns a non-negative random integer

```cs
Random random = new Random();

random.Next(); // Example: 665004238
random.Next(); // Example: 392976750
random.Next(); // Example: 1178083184
```

`Next(int)` - Returns a random integer between 0 and *less than* the specified maximum.

```cs
Random random = new Random();

random.Next(10); // Random number between 0 and 9
random.Next(51); // Random number between 0 and 50
random.Next(101); // Random number between 0 and 100
```

`Next(int, int)` - Returns a random integer between the lower bound and *less than* the specified maximum, or upper bound.

```cs
Random random = new Random();

random.Next(1, 11); // Random number between 1 and 10
random.Next(0, 10); // Random number between 0 and 9
random.Next(10, 101); // Random number between 10 and 100
```