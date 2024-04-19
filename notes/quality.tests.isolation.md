---
id: ntzttuecde32frbadleygwy
title: Test Isolation
desc: ''
updated: 1708453973978
created: 1708453964313
---

> Test should only fail because of the system under test.

Consider two cases. In the first case, you are testing your code under test which is independent. Now, if an error occurs in your test, you'd know it was because there is something wrong with your code.

Second case - your code depends on some other class or code. Now, if you get error in your unit test, you wouldn't know where the error is coming from. This makes the whole exercise of creating a unit test pointless. You'll still have to investigate which part is causing the error in your machinery despite the test.
