
Caller sends a request and waits for it to get completed. Meanwhile, caller is blocked and resumes only when the receiver responds.

Caller and receiver are in "sync".

## Example

- Program asks OS to read from disk
    - Program main thread is taken off of the CPU
    - Read completes, program can resume execution
- Phone call/meetings