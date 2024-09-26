
Caller sends a request and does other work while the receiver responds.

## How to know when request is ready?

- Polling
- Pushing
- A separate [[execution.synchronicity.sync]] thread that is blocked.


## Example

- File read
    - A secondary thread is spun-up to read this file
    - Main thread still in CPU, unblocked.
- Email