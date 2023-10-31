---
title: Dependency Injection
description: ""
date: 2023-10-31T11:00:38.097Z
preview: ""
draft: false
tags: []
categories: []
---

## What is Dependency Injection?

Everyone has heard "call down, signal up" in Godot. This is a good practice to follow, but it can be a bit cumbersome to implement in some cases. 

Dependency Injection is a design pattern that allows you to inject dependencies into your classes. This is useful for decoupling your code and making it more testable.

In Godot it allows to inject parent object references to children.

## How to use it?

Let's say that you have `Game` node and two nodes `Player` and `Enemy` as children. You want to
make `Enemy` to follow `Player` and you want to do it in `Enemy` script.

One option is to use raycasting and areas to determine when `Player` is in range and then start
following.

Another option is to use dependency injection. You can inject `Player` reference into `Enemy` and
then use it to follow `Player`.

To do that you need to add a script to common parent, in this case `Game` node. In this script you
pass reference to `Player` to `Enemy` node.

```gdscript
extends Node

func _ready():
    var player = get_node("Player")
    var enemy = get_node("Enemy")
    enemy.player = player
```

Then in `Enemy` script you can use `player` variable to follow `Player`.

```gdscript
extends Node2D

var player

func _process(delta):
    if player:
        position = position.linear_interpolate(player.position, delta * 2)
```

That simple.
