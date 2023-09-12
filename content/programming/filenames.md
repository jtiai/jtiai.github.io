---
title: "File and directory names"
date: 2023-09-12T20:51:03+03:00
draft: false
---

File and directory names should follow same rules as variable names. They
should be meaningful and descriptive.

The most important thing is that _everything must be lowercase_. This is because
Godot is case sensitive. If you have a file named `Player.gd` and you try to
load it with `load("player.gd")`, it will not work.

In many cases operating systems are case insensitive, but case preserving. This
means that if you have a file named `Player.gd` and try to rename it to
`player.gd`, it will not work. The file will still be named `Player.gd`. This
will lead issues later on and it's best to avoid it.
