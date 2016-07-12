# Building High Performance Daydream Apps
- Nathan Martz @NathanMartz
- Daydreaaaaaammmm

- Ear to eye 0ms
- in VR
  - Ear to cpu to gpu to display to eyes
- How to get low latency
- Rendering, Performance, Audio
- goo.gl/Hzk6Dd

- Unreal engine for VR now
- Unity for VR this summer

- Performance
  - Batch Counts
   - most common cause of CPU bottlenecks
   - Target 100 batches per eye (200 batches per frame)
   - Bake everything
     - combine local instances of static geometry
     - lightmap static geography
     - prerender background geometry
   - Beware the bus
     - tweak offscreen render texture size
     - always use compressed textures
     - avoid full screen passes
   - Prefer the vertex shader to the pixel shader
     - 20x fewer polygons than pixels
     - move logic from PS to VS where possible
     - Target ~100k verts per eye (~200 per frame)
   - 30Hz vs 60Hz
   - Stable framerate is key
     - evaluate both 30hz and 60hz
     - if running at 30hz use less than 33ms per frame
     Profile!
     - evaluate both CPU and GPU
     - make it a habit
     - Suggest with sound
   - Spatial Audio
     - use binaural model, not just stereo panning
   - environmental audio
     - location shapes the character of the sound

 ## Wrapping up
 - devside.googleplex.com/vr/concepts
