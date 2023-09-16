---
title: Scene Unique Names
description: ""
date: 2023-09-13T17:29:52.163Z
preview: ""
draft: true
tags: []
categories: []
---

Scene unique names are a way to identify nodes in a scene tree despite their
location in the tree. This is useful when you want to access a node from a
different node, but you don't know where it is in the tree.

## How to use

To use unique name on scene, you first need to set the name of the node in the
scene tree. You can do this by selecting the node in the scene tree and then
setting the name in the inspector.

Then select node in the scene tree, right click on it and select "Access as
Unique Name".
![Access as Unique Name](/images/scene-unique-names/access-as-unique-name.png)

This will mark the node as unique name and will add `%` sign to
denote that it is a unique name.
![Unique Name](/images/scene-unique-names/unique-name.png)

Now you can access this node from anywhere in the scene tree by using the
`get_node` function and passing the unique name as an argument and prefixing 
with a percent sign.

```gdscript
var node = get_node("%NodeName")
```

{{% notice tip %}}
Unique node names accessible globally throught the current scene. This means
that you can access unique node names from any node in the scene tree.
{{% /notice %}}
