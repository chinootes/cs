---
id: 9o86nbg2dro9c4zutzu7c9c
title: Class Cast Exception
desc: ''
updated: 1727010210373
created: 1727010208466
---

An exception occurs when a class which is not the superclass or which was not originally the superclass is casted.

For example, if Dog is casted to Cat. Or if Dog is upcasted to Animal and we try casting that Animal object to Cat.

It is advised to determine if the class you're downcasting is an instance of the class you're downcasting to.