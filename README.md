# Hello, I'm Caden Parker
C/C++ engineer focused on real-time graphics, performance, and systems-level work.

---

## Open-source Contributions

### three.js
- https://github.com/mrdoob/three.js/pull/32329 — Add float packing / unpacking intrinsics to TSL
- https://github.com/mrdoob/three.js/pull/32300 — Support struct definitions / declarations in TSL Transpiler
- https://github.com/mrdoob/three.js/pull/32272 — Fix invalid code generation in TSLTranspiler

## Graphics Projects

### 3D Cyclic Cellular Automata
A real-time 3D cyclic cellular automata simulation implemented with WebGPU compute shaders.

[CCA..webm](https://github.com/user-attachments/assets/17c2f292-b14a-42c1-8230-da49f015c98e)

#### Optimizations
- Uses a **(8, 4, 2)** 3D workgroup size to maximize cache-coherent reads along the X axis
- Bitpacks cell states to signifcantly reduce overall memory bandwidth
- Assigns multiple cellular automata states to a single GPU thread, improve memory re-use and ALU usage
- Rendered by rasterizing a bounding box and performing per-pixel DDA voxel traversal along the view ray
