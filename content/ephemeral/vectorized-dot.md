---
created: 2025-04-05
confidence level: low
review count: 0
---
- Creating a microkernel (or $\micro$-kernel) to compute the dot product efficiently using SIMD (Simple Instruction, Multiple Data).
- In SIMD programming, a microkernel is a small, highly optimized compute kernel that handles a core computational task (dot product, matrix multiply, or a small tile of a larger matrix operation). It's designed to run in tight loops, maximize use of CPU registers, SIMD instructions, and caches, be reused/composed into bigger kernels. In this context it's just a small function/routine that performs a specific computation on a portion of data, usually in a data-parallel way. It's often written to be run many times, one per element, or block of elements in a dataset.
- **tl;dr**: A microkernel is a small, focused, performance-critical function/routine that does the same operation on a bunch of data usually in parallel.
- A compute kernel is basically any function that performs a specific computation, usually parallelizable. This can be big or small e.g. a block of GEMM, or a full dot product.
- A microkernel is a small tightly optimized compute kernel, typically at the innermost loop level, tuned for a specific architecture. It's a subset of compute kernels.
-  Another way to think of it is that a compute kernel is the general unit of computation while a microkernel is a special case; it's the core, ultra-optimized tile inside that unit.
- Using GEMM as an example, 