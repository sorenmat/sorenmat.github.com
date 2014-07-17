---
layout: post
title: Aggregates
quote: The bread and butter of software developement
image: false
video: false
---


# Building blocks of Domain Driven Design (DDD)

This post will describe the main building blocks of domain driven design (Aggregates, Entities and Value Objects)

## Entities

Are objects that are defined by their identity (id). An example of this could be a ticket to a movie, it's identity is the row / seat number.

One of the more common "mistakes" in DDD, is to define to many objects as entities, so be aware of this pitfall.

## Value objects

This type of objects is defined by their attributes / values, and not by an identity. Value objects are immutable. An example of a value object could be a dollar bill, you generally only care about it as a $5 bill (it's value) and not by it's uniquely identifier. Another example could be an address object, if it's the same address you don't care if you get object A or object B.

## Aggregates

An aggregate is a cluster of related objects, controlled through a root entity (Aggregate root).

The classic example of an aggregate is an order that have some orderlines. It is the graph of those entities and value objects that is the aggregate.

It is the responsibility of the aggregate root to keep the data in the cluster of objects consistent. References from outside my only point to the aggregate root and only the aggregate root. All modification to the aggregates objects must go through the aggregate root.

The aggregate has a transactional boundary, so modifications should only modify one aggregate in a given transaction.

### Why should I use aggregates ?
Aggregates give you a nice way to keep logic where it belongs. You can think of the aggregate root as being an interface / API to the cluster of objects it controls.

The aggregate pattern gives you the ability to use the repository pattern, which will be discussed in another post.



