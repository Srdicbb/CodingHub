# The Compilation Chain

> Phase 8.1 | Status: Partial | Priority: LOW

## Current Knowledge

- Wrote Linux kernel drivers and FPGA code at RT-RK - understand low level
- Know the .NET compilation chain from daily work
- Discussed machine code vs high-level languages with friends

## Examples / Notes

### Machine Code & Assembly
- Machine code = binary instructions CPU executes directly
- Assembly = human-readable 1:1 mapping to machine code
- You worked with both at RT-RK (Linux drivers, character drivers)

### Compilation Chains
- TODO: .NET: C# -> IL (Intermediate Language) -> JIT -> Machine code
- TODO: Java: Java -> Bytecode -> JVM JIT -> Machine code
- TODO: Go: Go -> Machine code (ahead-of-time compiled)
- TODO: JavaScript: Interpreted -> JIT compiled (V8 engine)
- TODO: Rust/C/C++: Source -> Machine code (compiled, no runtime)

### Why High-Level Languages Exist
- Languages are for HUMANS, not computers
- Computers only understand binary - everything else is abstraction
- Abstraction exists for maintainability, team collaboration, portability

### Why AI Won't Write Machine Code Directly
- TODO: Machine code is CPU-specific (x86, ARM) - not portable
- TODO: The bottleneck is design and architecture, not language
- TODO: Maintainability requires human-readable code

## Questions / Confusions

- How does JIT compilation decide what to optimize?
- What's the performance difference between JIT and AOT compilation?
- Could future AI models generate optimized IL/bytecode directly?
