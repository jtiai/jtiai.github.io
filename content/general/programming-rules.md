---
title: "Programming Rules"
date: 2023-09-11T09:02:09+03:00
draft: false
weight: 2
---

These are some rules I use when writing code. They are not set in stone and
they are not the only way to do things. They are just my way of doing things.

## 1. Use meaningful names

Use names that describe what the variable, function, or node is used for. For
example, if you have a variable that holds the player's score, you can name it
`player_score`. If you have a function that calculates the player's score, you
can name it `calculate_player_score`. If you have a label node that holds the
player's score, you can name it `PlayerScoreLabel`.

## 2. Use comments

Use comments to explain what the code does. For example, if you have a function
that calculates the player's score, you can add a comment that explains how the
score is calculated.

## 3. DRY - Don't Repeat Yourself

Every source of information should have a single, unambiguous, authoritative
representation within a system. For example, if you have RPG player statistics
like strength, dexterity, and intelligence, you can create a `PlayerStats`
resource that holds all the information about the player's stats. Then you can
use that resource in all the places where you need to access the player's stats.

Don't repeat yourself is not about avoiding repetition. It's about avoiding
duplication. It's about avoiding duplication of knowledge.

## 4. YAGNI - You Ain't Gonna Need It

Don't add functionality until you need it. For example if you have a game
where the player can move left and right, you don't need to add jumping until
you need it.

## 5. Premature Optimization is the Root of All Evil

Don't optimize your code until you need to. For example, if you have a game
where the player can move left and right, you don't need to optimize the
movement code until you need to.

And when you face a performance problem, don't optimize the code that you think
is slow. Instead, profile your code to find out what is actually slow. Then
optimize that code.

## 6. Rule of Three

If you need to do something more than three times, you should create a function
or a node that does that thing. For example, if you need to calculate the
player's score more than three times, you should create a function that
calculates the player's score.
