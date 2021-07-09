# LLVM
Compilers translate code written in programming languages like C, C++ to assembly instructions.
Compilers have optimization tricks like constant folding, function inlining etc.
However traditional compilers are monolithic and it is hard to add more optimizations.

LLVM compilers are modular and new optimizations can be added.

LLVM helps reduce this gap with the ability to create LLVM IR, intermediate representation.
.c -> .ll -> .asm

This .ll code undergoes multiple cycles of transformations until no more optimizations are possible.
LLVM takes this platform generic .ll code and converts it to platform specific (X86, ARM, RISC ..) assembly code.

With high level programming languages like Swift which does memory management as well, there is a huge gap between the programming language code and the 
assembly.
To address this, Swift has one more intermediate step.

Swift -> SIL -> LLVM IR -> .asm

