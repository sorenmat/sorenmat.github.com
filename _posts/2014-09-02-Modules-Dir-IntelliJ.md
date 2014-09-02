---
layout: post
title: Setting modules dir as default
quote: How to set the module dir as default directory in IntelliJ
image: false
video: false
tags : [intellij]
---

When running code from IntelliJ i often run into the issue, that my project file is not located in the same directory  as the code. This will mess up code that are looking for locale files since the don't exists in the project directory.

The solution is quite simple and easy, but for some reason it has taken me for ever to find it.

You have to go the edit run / debug configuration, and go under the defaults. Find e.i. JUnit, and enter $MODULE_DIR$ in the working directory field. This will use the module directory as the default value when creating new JUnit run / debug configuration.

Easy and simple :)

