---
id: ckytr8qz9uyrfyzrtmmf2c6
title: Data Access Object
desc: ''
updated: 1708452486060
created: 1708452468407
---

Its a [[arch.design.oo.patterns]] in which the data access object (DAO) is an object that provides an abstract interface to some type of database or other persistence mechanism. By mapping application calls to the persistence layer, DAO provide some specific data operations without exposing details of the database.

Basically, ek class bana do StudentDAO type. Usme sab function rahega insert, get ye wo operation database mein karne ke liye. Fir kisi aur class se ye sab function ko directly value pass karo bass. This way, database mein peechhe kya chal raha is abstract.
