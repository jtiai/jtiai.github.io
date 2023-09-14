---
title: "Signals"
date: 2023-09-14T10:14:08+03:00
draft: false
---

Godot signals are a way to send messages between objects. They are similar to events in other programming languages. Main use for signals is to decouple objects from each other.

In Godot most common usage of signals to to notifify nodes that
are not children of the current node. 

In short: signal up, call down.


## Declaring signals

Signals are declared in the script using `signal` keyword. Signals are declared in the same way as methods, but without body. 

```gdscript

signal my_signal

signal takes_param(some_param)
```

## Emitting signals

Signals are emitted using `emit()` method. 

```gdscript

my_signal.emit()

```

Note: Godot doesn't check sigal signature. It is possible to emit signal with wrong number of parameters.

## Connecting signals   

Connecting signals is done using `connect()` method on signal itself. `connect()` takes `Callable` as a parameter. `Callable` is a special type that can be used to call functions. In most cases is name a function (no quotes, no parentheses). 

```gdscript

some_instance.my_signal.connect(_on_my_signal)

```

