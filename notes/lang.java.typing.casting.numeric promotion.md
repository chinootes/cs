---
id: k20g1bpp5x7ol75d8eafwp5
title: Numeric Promotion in Inter-type operations
desc: ''
updated: 1712883921435
created: 1712883885609
---

It is necessary both numeric operands are compatible in size in an operation. If not, they're converted.

Here's how that happens (Rules)

- If one operand is double, float or long

    the other promoted to double, float or long respectively

- Else

    both are considered int
