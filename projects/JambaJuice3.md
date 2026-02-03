---
layout: project
type: project
image: img/cotton/JambaJuice.png
title: "Jamba Juice Menu & Order System"
date: 2026
published: true
labels:
  - TypeScript
  - Object-Oriented Programming
  - Software Engineering
summary: "A TypeScript-based system that models Jamba Juice menus, customer orders, and store inventory."
---

<img class="img-fluid" src="../Users/kimsunwoo/Documents/GitHub/kimseonw07.github.io/img/cotton/Jamba-Juice-3317b5815056a36_331852ed-5056-a36a-0824955f2c2f23c8.jpg">

This project is a TypeScript implementation of a simplified Jamba Juice store system, developed as part of a series of WODs (Workout of the Day) in ICS 314. The project incrementally models real-world entities using object-oriented design principles.

The system begins by representing Jamba Juice menu items, including their ingredients, prices, and calorie counts by size. It then extends this functionality to support customer orders and, finally, store inventory management.

In **Jamba Juice 1**, I implemented:
- A `MenuItem` class to represent individual drinks
- A `Menu` class to store menu items and search for drinks by ingredient

In **Jamba Juice 2**, I added:
- A `Drink` class to represent a specific drink order with a selected size
- An `Order` class to manage multiple drinks and compute the total cost

In **Jamba Juice 3**, I extended the system to reflect real-world constraints:
- An `Inventory` class to track available servings of each ingredient
- A `Store` class that produces drinks while decrementing inventory and preventing orders when ingredients run out

This project emphasizes:
- Strong type safety using TypeScript features such as union types, generics, and `Record`
- Incremental design and extension of an existing codebase
- Modeling realistic constraints in software systems

Source:  
<a href="https://www.typescriptlang.org/play/"><i class="large github icon"></i>TypeScript Playground</a>
