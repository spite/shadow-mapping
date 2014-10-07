Shadow mapping shader
=========
---

Demo: [Shadow mapping](http://www.clicktorelease.com/tmp/threejs/shadow-mapping)

Implementation of shadow mapping in GLSL for three.js

  - Fixed directional light (fixed ambient and light colour)
  - Averaged and poison-disk sampling averaged
  - Projector

This is done with the purpose of exploring the different shadow-mapping techniques, and having a more-or-less correct solution to use when creating my own shaders. In three.js right now it's not immediate to mix custom shaders and default material features.

License
----

MIT