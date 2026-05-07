---
layout: project
type: project
image: img/cotton/JambaJuice.png
title: "Jamba Juice Store System"
date: 2026
published: true
labels:
  - TypeScript
  - Object-Oriented Programming
  - Software Engineering
summary: "A TypeScript system modeling a real-world Jamba Juice store — menus, customer orders, and live inventory management — built incrementally across three stages."
---

<img class="img-fluid" src="../img/cotton/Jamba.jpeg">

## Overview

This project is a TypeScript implementation of a simplified Jamba Juice store, developed as a series of incremental exercises in ICS 314. Starting from a basic menu representation, the system grows to support customer orders and, finally, live inventory management that prevents orders when ingredients run out. Each stage adds new classes and constraints on top of the previous one, simulating how real-world software evolves.

## What I Built

**Stage 1 — Menu modeling:** Designed a `MenuItem` class representing individual drinks with ingredients, prices by size, and calorie counts. Added a `Menu` class that stores items and supports ingredient-based search.

**Stage 2 — Order management:** Extended the system with a `Drink` class to represent a sized drink selection, and an `Order` class that manages multiple drinks and computes a running total cost.

**Stage 3 — Inventory constraints:** Introduced an `Inventory` class tracking available servings of each ingredient, and a `Store` class that decrements inventory as drinks are produced and rejects orders when stock runs out — modelling realistic operational constraints.

## What I Learned

This project was my first hands-on experience with TypeScript's type system at meaningful depth. Using union types to represent drink sizes, generics for flexible container types, and `Record` for ingredient tracking forced me to think carefully about data shapes before writing any logic. I also learned how to design classes that compose cleanly — each stage required extending existing code rather than rewriting it, reinforcing the value of forward-compatible design from the start.

Source: <a href="https://www.typescriptlang.org/play/"><i class="large github icon"></i>TypeScript Playground</a>
