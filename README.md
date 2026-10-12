Shadow mapping shader
=========

Demo: [Shadow mapping](http://www.clicktorelease.com/tmp/threejs/shadow-mapping)

Implementation of shadow mapping in GLSL for three.js

  - Fixed directional light (fixed ambient and light colour)
  - Depth packed into an RGBA render target, with slope-scaled bias
  - Averaged or Poisson-disk sampling (uncomment `#define POISSON_DISK` in the `shadow-fs` shader to switch)
  - Projector

This is done with the purpose of exploring the different shadow-mapping techniques, and having a more-or-less correct solution to use when creating my own shaders. In three.js right now it's not immediate to mix custom shaders and default material features.

The geometry doesn't have to be merged: the shadow coordinates use each mesh's modelMatrix, so any mesh in the scene casts shadows and any mesh using the shadow material receives them. The demo still merges its geometry into a single mesh to keep it to one draw call. Don't use this code for anything else than playing around!

License
----

MIT