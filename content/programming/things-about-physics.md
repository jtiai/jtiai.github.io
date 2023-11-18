---
title: Things About Physics
description: ""
date: 2023-11-18T17:19:53.455Z
preview: ""
draft: true
tags: []
categories: []
---

## Some random things about physics in Godot

### Physics bodies vs. Areas

`StaticBody2D`, `RigidBody2D`, and `CharacterBody2D` and theird 3D equivalents
`StaticBody3D`, `RigidBody3D`, and `CharacterBody3D` are physics bodies. They
are used to detect collisions and apply forces to other bodies.

`Area2D` and `Area3D` are used to detect overlappings.

Difference is that when physics bodies detects collision they do give you
options to determine what to do with information about collision. By default
for `CharacterBody` you can use `move_and_sllide` and it automatically detects
collisions and reacts to them, like stopping when hitting wall or sliding down.

`Area2D` and `Area3D` are used to detect overlappings. They don't give you any
information about collision, they just tell you that something is overlapping
with them. You can use them to detect when player is in range of enemy or when
player is in range of item to pick up.

{{% notice warning %}}
Do not nest physics bodies inside of each other. This can cause unexpected
behavior.
{{% /notice %}}

### Physics layers and masks

This is the most confusing part of physics in Godot.

Layers and masks are used to determine how physics bodies interact with each
other. You can set layers and masks only for each physics body, not for shapes.

Layers tells in Godot which layers physics body belongs to. You can set up to
32 layers.

Masks tells in Godot which layers physics body can collide with. In other words
which layers it can interact with. You can set up to 32 masks.

For example if your game has 4 physics objects `Player`, `Enemy`, `Bullet`,
and `Fence`. You want `Player` to collide with `Enemy` and `Fence` but not with
`Bullet`. You want `Enemy` to collide with `Player`, `Fence` and bullet but
not with other `Enemy`. You want `Bullet` to collide with only `Enemy`, not with
`Player` or `Fence`. `Fence` doesn't need to collide with anything.

You can set up layers and masks like this:
`Player` layer 1, masks 2 and 4
`Enemy` layer 2, masks 1, 3, and 4
`Bullet` layer 3, masks 2
`Fence` layer 4, masks 0

{{% notice tip %}}
You can name collision layers in `Project Settings -> Layer Names`
{{% /notice %}}
