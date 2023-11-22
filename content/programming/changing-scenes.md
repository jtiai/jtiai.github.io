---
title: Changing Scenes
description: ""
date: 2023-11-21T22:33:58.128Z
preview: ""
draft: false
tags: []
categories: []
---

## Changing Scenes

Godot has multiple ways to change the scene. The most common way is to use `change_scene_to_packed` or `change_scene_to_file` method.

Usage of `change_scene_to_packed`:
```
var next_scene = preload("res://levels/level2.tscn")

func _on_Button_pressed():
    get_tree().change_scene_to_packed(next_scene)
```

Usage of `change_scene_to_file`:
```gdscript
func _on_Button_pressed():
    get_tree().change_scene_to_file("res://scenes/Level1.tscn")
```

## More complex scene changing

When you want to keep `Player` or some other game data between scenes you can
use previously mentioned methods with Godot autoload system.

Another system is to have `Game` node that is always present in the scene tree.

Create a node tree like this:

![Scene tree](/images/changing-scenes/scene-tree.png?classes=left)

Then add a script to `Game` node and add this code to it:

```gdscript
extends Node

const LEVELS = [
    preload("res://levels/level1.tscn"),
    preload("res://levels/level3.tscn"),
    preload("res://levels/level3.tscn"),
]

var current_level = -1

func _ready() -> void:
    next_level()

func next_level():
    # Remove previous level
    for node in $Level.get_children():
        node.queue_free()

    # Instantiate and add new level
    current_level += 1
    var new_level = LEVELS[current_level].instantiate()
    $Level.add_child(new_level)
```

Now when you want to change a level just call `next_level` function in `Game` node.
