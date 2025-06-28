A scheme to x86 compiler in about 500 lines of code!

A few lines of code more and I can print the x86 text a run it!

;;;

An interesting observation is this.

In my program, I have only defined 

- `movq`
- `addq`
- `subq`
- `cmpq`

So, the CPU is just moving data from the stack to register, register to stack, register to register and increasing the program counter, but never from stack to stack. And the processor is comparing and adding or subtracting.

In addition to these four x86 instructions, I can add a few more and that's enough for the CPU to execute a small Scheme compiler.

So, the purpose of the a-normalization pass is to translate the source language into another one such that the data is readily available in
either the stack or registers.

