---
id: 3vkrzzyai2q6d13i1cu8g6s
title: Template Method
desc: ''
updated: 1708452794899
created: 1708452769178
---

[[arch.design.oo.patterns.gof.behavioural]]

## Goal

When you need to define certain steps in a particular order, but the internals of those steps can vary.

## Solution

Create a superclass (usually an abstract superclass), with a method containing the steps in the desired sequence. These steps will be in form of methods, which the subclasses can choose to skip or implement in the specific way.

## References

[Template Method Design Pattern - Derek Banas](https://youtu.be/aR1B8MlwbRI?si=8QIkWnMnCegYec3A)