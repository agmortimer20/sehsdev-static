---
title: Algorithm - Divisibility
---

[← Back](/references/)

### Introduction

To find out whether a number is even, odd, or merely divisibile by another number, we need to do a little bit of long division.

A few things to recall:
- When performing long division, there are two parts to an answer: the *quotient* and the *remainder*.
    - The quotient is the number of times the *divisor* goes evenly into the *dividend*.
    - The remainder is the leftover value, or what value remains after a quotient is derived.
- If a number divides evenly into antoher number, the remainder is *zero*.
- Even numbers are divisble by two, odd numbers are *not* divisible by two.

### Language

1. [JavaScript](#JavaScript)
2. [C#](#c-sharp)

### JavaScript

```js
console.log(`Is 10 divisible by 3? ${10 % 3 == 0}`)
console.log(`Is 10 divisible by 2? ${10 % 2 == 0}`)

// Even or Odd?

if (10 % 2 == 0) {
    console.log("10 is even")
}
else {
    console.log("10 is odd")
}

if (13 % 2 == 0) {
    console.log("13 is even")
}
else {
    console.log("13 is odd")
}

```

<h3 id="c-sharp">C#</h3>

```cs
Console.WriteLine($"Is 10 divisible by 3? {10 % 3 == 0}");
Console.WriteLine($"Is 10 divisible by 2? {10 % 2 == 0}");

// Even or Odd?

if (10 % 2 == 0) {
    Console.WriteLine("10 is even");
}
else {
    Console.WriteLine("10 is odd");
}

if (13 % 2 == 0) {
    Console.WriteLine("13 is even");
}
else {
    Console.WriteLine("13 is odd");
}
```