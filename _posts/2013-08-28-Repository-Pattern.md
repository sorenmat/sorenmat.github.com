---
layout: post
title: Repository pattern
quote: Please daddy, save my stuff
image: false
video: false
---


# Repository pattern

The basic idea of the repository pattern is to seperate buisness logic and persistence logic through a list like sematic.

The great thing about this, as asposded to the way orm's does things is that you force the developer to think about when and how do i access data.You just can't navigate around in the model, and expect some framework to handle it magiccally for you. 


The idea of a repository teams up well with aggregates. Imagine the repository as an interface of List[Aggregate], where you can add, remove, delete etc. from.
