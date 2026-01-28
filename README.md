# Hello, I'm Caden Parker
C/C++ engineer focused on real-time graphics, performance, and systems-level work.

---

## Open-source Contributions

### three.js
- https://github.com/mrdoob/three.js/pull/32329 — Add float packing / unpacking intrinsics to TSL
- https://github.com/mrdoob/three.js/pull/32300 — Support struct definitions / declarations in TSL Transpiler
- https://github.com/mrdoob/three.js/pull/32272 — Fix invalid code generation in TSLTranspiler

## Projects

### [3D Cyclic Cellular Automata](https://github.com/Ne0nWinds/3D-Cyclic-Cellular-Automata)

A real-time 3D cyclic cellular automata simulation implemented with WebGPU compute shaders

![ezgif com-video-to-webp-converter-5](https://github.com/user-attachments/assets/93320e16-a6bf-4a34-ab4d-e41893b28143)
![output](https://github.com/user-attachments/assets/eb97a1dc-a582-4c94-b6ff-41d1137798bd)


#### Optimizations
- Uses a **(8, 4, 2)** 3D workgroup size to maximize cache-coherent reads along the X axis
- Bitpacks cell states to signifcantly reduce overall memory bandwidth
- Assigns multiple cellular automata states to a single GPU thread, improve memory re-use and ALU usage
- Rendered by rasterizing a bounding box and performing per-pixel DDA voxel traversal along the view ray


### [SIMD Ray Tracer](https://github.com/Ne0nWinds/SIMD-Ray-Tracer)

A brute-force ray tracer, optimized with SIMD and multi-threading

<img width="480" alt="image" src="https://github.com/user-attachments/assets/eba493e4-0657-4ba2-be30-56c2f13e87a4" />

Live Demo: https://simd-ray-tracer.netlify.app/

#### Key Features
- Compiles to WASM and x64, supporting WebAssembly SIMD, SSE2, and AVX2
- Data is layed out in an array of struct of arrays, ensuring good cache locality and compatibility with SIMD
- Supports matte, specular, and fresnel materials
