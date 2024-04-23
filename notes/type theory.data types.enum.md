---
id: eriko0qvndg5mlp8gr9umek
title: Enum (Enumerated Types)
desc: ''
updated: 1713902292806
created: 1708541155869
---


Data type consisting of a set of named values called elements, members, enumeral, or enumerators of the type. The enumerator names are usually identifiers that behave as constants in the language.

## Usage

Where fixed set of constants or ranges are required

## Examples

- the four suits in a deck of playing   cards may be four enumerators named *Club, Diamond, Heart, and Spade*, belonging to an enumerated type named *suit*. If a variable V is declared having suit as its data type, one can assign any of those four values to it.
- range of phones/laptops, colors, seasons, days of week.

## Isn't it [[type theory.data types.literal]]?

While enums, like literal limit the set of values possible for a variable, they are not literal.

Enums group together [[type theory.data types.literal]]s and give them semantic meaning.
