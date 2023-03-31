# Rust Gamedev
My curated list of cool/useful crates for game development. Crates often have strange names that are difficult to remember or do not make it obvious what they do. This repository is where I keep track of crates I've found that may be useful for certain problems or projects.

| Crate | Description |
| ----- | ----------- |
| [crunch](https://crates.io/crates/crunch) | space-efficient rectangle packer |
| [delaunator](https://crates.io/crates/delaunator) | triangulation of 2D points, good for mesh/collider gen, or any procedural stuff like that |
| [arboard](https://crates.io/crates/arboard) | text/image clipboard support, useful for editors/etc. especially because of the image support |
| [bincode](https://crates.io/crates/bincode) | very fast + compact binary serializer, output is nearly same size as in-memory structs, great for simple inline serialization |
| [strum](https://crates.io/crates/strum) | add lots of reflection to enums (names, count, enumerate over their values, etc.), great to remove boilerplate and prepare enums for in-editor dropdown support |
| [glam](https://crates.io/crates/glam) | my current favorite of the fast linear algebra (vectors, matrices, etc.) crates, designed for games/graphics, and has some SIMD-support |
| [euc](https://crates.io/crates/euc) | simple and to-the-point software renderer, good for debugging or tooling, and also as studying material |
| [glow](https://crates.io/crates/glow) | nice OpenGL bindings/wrapper |
| [glsl](https://crates.io/crates/glsl) | glsl 450/460 parser, which creates a syntax tree out of opengl shader code, very simple to use and navigate |
| [lyon](https://crates.io/crates/lyon) | very nice path tesselation library, for generating meshes from vector contours/paths |
| [msdf](https://crates.io/crates/msdf) | generate multi-signed distance fields out of contours, good for generating + baking textures for fast, scalable fonts |
| [rfd](https://crates.io/crates/rfd) | rust file-dialogs, useful for native save/load/etc. for editors and tooling |
| [strsim](https://crates.io/crates/strsim) | "string simularity" metrics, useful for fuzzy text searching (eg. in an editor when you want to search assets/sprites/etc.) |
| [ulid](https://crates.io/crates/ulid) | i like this for guid generation, which uses the [ulid](https://github.com/ulid/spec) specification to generate 128-bit unique IDs that have nice string representations |
| [wgpu](https://crates.io/crates/wgpu) | extremely powerful+sophisticated web-gpu cross platform rendering library, can output to metal/vulkan/dx/wasm, has its own shader language. the whole deal, very good |
| [naga](https://github.com/gfx-rs/naga) | great companion to wgpu, a shader parser that can parse and translate shaders. i've found it useful for evaluating shaders to automate some of the graphics code, as well as validating shaders' compatibility for engines/targets |
| [winit](https://crates.io/crates/winit) | the de-factor windowing library for rust, quite good compared to what i've used in any other language. feels very much like using SDL |
| [thiserror](https://crates.io/crates/thiserror) | my favorite library for creating error structs/enums with nice display implementations (reduces lots of boilerplate and can generate from-impls as well, etc.) |
| [bytemuck](https://crates.io/crates/bytemuck) | library with traits/methods for making your structs readable/writable as byte arrays, useful for uploading them into graphics APIs like wgpu or opengl |
| [memoffset](https://crates.io/crates/memoffset) | nice companion to bytemuck, allows you to get memory offsets of struct fields, useful for setting up vertex attributes or uniform buffers for graphics APIs |
| [gilrs](https://crates.io/crates/gilrs) | gamepad input library, really great API, controller layout/bindings/event handling, and haptic support |
| [image](https://crates.io/crates/image) | very full-featured image decoding library with support for lots of common formats |
| [png](https://crates.io/crates/png) | the `image` crate is very large, so for merely PNG support, using this directly makes for a faster compile and smaller dependency footprint |
| [approx](https://crates.io/crates/approx) | floating point approximation, great for those times where pesky f32's are deciding to be never quite equal. should be used in place of direct equality checking as often possible |
| [rand_xoshiro](https://crates.io/crates/rand_xoshiro) | very nice random number generators, i specifically like `SplitMix64` for being very simple, fast, and with a simple 64-bit state, but it has more sophisticated generators available as well |
| [rusttype](https://crates.io/crates/rusttype) | great for parsing and rasterizing opentype fonts and generating glyph sets for rendering.