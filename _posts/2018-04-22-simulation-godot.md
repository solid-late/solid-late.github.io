---
layout: post
title: Simulating the LED patterns with the Godot game engine
date: 2018-04-22
category: drafts
authors: aleks
---

While the 3D prototype was being built and we were waiting for our order to be delivered, we created a simulation for the lighting. We wanted to think about the possible patterns in advance to make it easier to adapt them to the Arduino later. 
We took a look at 10 white and 10 red LEDs we found and ordered on the list.
Unfortunately the try with [PythonQt](http://pythonqt.sourceforge.net/) and [kivy](https://kivy.org/) took a lot of time and was aborted to create the simulation with [Godot](https://godotengine.org/), an open source game engine.

In the following 8 different modes are shown.

![godot-reindeer](/static/img/godot-reindeer/godot_reindeer.gif)

### [The code can be found in the repository.](https://github.com/solid-late/godot_reindeerLED)