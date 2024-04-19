---
id: vcivgdtzkdtmstqf2d03714
title: Asynchronous
desc: ''
updated: 1708850181054
created: 1708847687880
---

Caller sends a request and does other work while the receiver responds.

## How to know when request is ready?

- Polling
- Pushing
- A separate [[execution.sync]] thread that is blocked.


## Example

- File read
    - A secondary thread is spun-up to read this file
    - Main thread still in CPU, unblocked.
- Email