

# aka Activation Record

Stack frame is created for function calls. A new one is created each time a function is called.

## Components

### Function Return Address

The return address (memory address) of the instruction to execute after the function call completes.

Pushed onto the stack first.

### Function Arguments

Space for function arguments (parameters) passed to the method.
Followed by any local variables.

### Local Variables

Variables declared within the method.
Allocated space for these variables.

### Frame Pointer (Optional)
Some architectures use a frame pointer (FP) to point to the start of the stack frame.

Helps access local variables and function arguments efficiently.

Not always present (depends on the calling convention).


## Lifecycle

### Function Call

When a method is called, a new stack frame is pushed onto the call stack.

The return address, arguments, and local variables are set up.

### Function Execution

The method executes, accessing its local variables and performing computations.

### Function Return

When the method completes, its stack frame is popped from the stack.

The return address is used to continue execution from where the method was called.
