---
title: Activity 1.5 Manipulating Variables
permalink: /activities/javascript/1-5
---

[← Back](/activities/javascript/)

### Introduction

This activity will take you a little bit deeper into how variables can be used. While the programs below are merely simulations, they will demonstrate how variables can have their values changed. Here are a few things you need to understand:
- The equal sign is called the assignment operator in programming. It is used to save, or assign a value to a variable.
    - We can overwrite a variable’s *existing* value using the assignment operator.


#### Skills to Practice

- Manipulate variable values

### Activity Instructions

#### Setup

1. Create a new repl.
    1. Select *Node.js* for the language.
    2. Name the Repl "*1.5 Manipulating Variables*".
2. Click Create repl.

#### Code
```js
// Video game demo
console.log("--- Battle Simulator ---")
var playerHealth = 100
var enemyHealth = 100
var enemyAttackDamage = 20
var potions = 3

console.log(`Health: ${playerHealth}`)
console.log(`Enemy health: ${enemyHealth}`)
console.log()

console.log("Round 1")
console.log("Player attacks.")
// Subtract 15 from enemyHealth. Save new enemyHealth value.
enemyHealth = enemyHealth - 15
console.log(`You did 15 damage! Enemy health: ${enemyHealth}`)
// Subtract enemyAttackDamage from player health. Save new playerHealth value.
playerHealth = playerHealth - enemyAttackDamage
console.log(`Enemy did ${enemyAttackDamage} damage! Player health: ${playerHealth}`)
console.log()

console.log("Using potion...")
playerHealth = playerHealth + 10
potions = potions - 1
console.log(`Player health: ${playerHealth}. Potions left: ${potions}`)

console.log("Buying one potion...")
potions++ // Increment operator - Increases number value stored in variable by one
console.log(`Potions left: ${potions}`)
console.log(`Using the potion!!!`)
potions-- // Decrement operators - Decreases number value by one


console.log("\n\n") // What does this do??? Google search "\n javascript"


// Bank account demo
console.log("--- Banking Simulator ---")
var accountName = "Checking Account"
var accountBalance = 100.50

console.log(`${accountName} balance: $${accountBalance}`)
console.log(`Depositing $99.01 to ${accountName}`)
accountBalance = accountBalance + 99.01
console.log(`${accountName} balance: $${accountBalance}`)
```

#### Debug

```shell
--- Battle Simulator ---
Health: 100
Enemy health: 100

Round 1
Player attacks.
You did 15 damage! Enemy health: 85
Enemy did 20 damage! Player health: 80

Using potion...
Player health: 90. Potions left: 2



--- Banking Simulator ---
Checking Account balance: $100.5
Depositing $99.01 to Checking Account
Checking Account balance: $199.51
```

### Tips, Tricks, and Reflection

- Remember that variables need to be spelled exactly the same every time.
- Make sure to use the right data type for your variables. When performing math, use numbers, not strings.
