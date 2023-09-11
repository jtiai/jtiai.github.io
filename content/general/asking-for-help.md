---
title: "Asking for Help"
date: 2023-09-11T09:01:49+03:00
draft: false
weight: 1
---


Asking for help in the best way possible is not as easy as when you need to
ask help by using computer. You only have a few tools at your disposal - text,
images and videos. It's also difficult to express yourself if you don't know
the exact terms or you don't know what happens on your computer or in your 
program.

## Where to ask for help?

The probably fastest and most modern way to ask for help is to use
the [Godot Discord server](https://discord.gg/4JBkykG)

Godot also has other help channels and resources which you can find
at https://godotengine.org/community/

## What are you trying to do?

The first thing when asking for help is to explain what are you trying to do.
It is a common pitfall to ask how to do "thing X". A single sentence is often
enough. The purpose is to give people helping you an overview and context of
your problem without technical details. For example:

- I'm trying to move my player from left to right.
- I'm trying to place multiple copies of my enemy on screen.
- I'm trying to make my player character jump.
- I'm trying to make enemy movement random.

## How are you trying to do that?

If you don't know how to achieve what you are trying to do, please say that.
It's as simple as saying: "I don't know how to do that". There is nothing
wrong with admitting that you don't know things - it's perfectly normal.

If you do have actual code that doesn't work *do not use screen captures*.
Your code isn't image, right? So you should copy your code exactly as is and
paste it into the proper place.

If your code is relatively short you can paste it into Discord. Put the code
between triple backticks (```````). If the code is written in python you can
add the word "swift" after first triple backticks and Discord highlights the 
code. Note that at the time of writing Discord doesn't have highlighting for
GDScript.

For example the following:

    ```swift
        for a in b:
            print(a)
    ```

Will render as (colors may vary):

```swift
    for a in b:
        print(a)
```

Why is this important? Because when you paste properly, people helping you
can copy and run the code on their machines. They can't copy text from images,
right?

If your code is longer and doesn't fit in Discord (Discord has some limit for
paste) you can use so-called pastebins for your code. If you have a GitHub 
account you can use [github gists](https://gist.github.com/) or there exists
several nice existing services like https://dpaste.org/ where you can paste 
your code as well.

If you have a full project sharing it by using distributed repositories is a
good option like using [GitHub](https://github.com/), [GitLab](https://gitlab.com/), or
[BitBucket](https://bitbucket.org/).

## Error messages

If you encounter an error message may have a lot of useful
information for people helping you. You should copy-paste it as is because
it can show the problem immediately. It's okay if you want to strip off some
leading paths for example revealing your account name.

## Problems with output

If you have problems that are only visible on display only there are a few
options how to handle that. If the problem can be shown in a still image,
a screen capture is a good option. On most computers it is enough to press
`Print Screen` button to have a screen captured.

If the problem requires recording a video, you need to have some tool for
recording videos. One such a tool is [ScreenToGif](https://www.screentogif.com/) 
which is a free, open source tool for capturing video to gifs.

## Tutorials

If you are following a tutorial and you have problems with it, you should
mention the tutorial you are following. It's also a good idea to mention
the exact place where you are having problems. For example: "I'm following
the tutorial at https://docs.godotengine.org/en/stable/getting_started/step_by_step/your_first_game.html
and I'm having problems with the part where I'm supposed to add a new node."
