# Engineering Cinematic Experiences in VR
## Wednesday May 18, 2016
Speakers
- Andrew Scherkus
- Husain Bengali
- Dillon Cower

## Spacial Audio
- Jump
  - VR video creation program

### Video Projections and Playback
- needs stereo resolution
- no buffering ever ever ever

### How to create immersion
1. Pick a sphere to plane projection to represent 360 video
2. increase video resolution until pixels >= display + optics
3. double resolution to stereo

### Approximating Resolution
- 2560 horizontal pixels/ 2 eyes = 1280 px
- 1280 pix / 100 degrees field of view = 12.8 physical
- ... more math ...

- mono = 10.6mp for mono
- 21.2mp for stereo
- 8.3 is for 4K

### Projection Challenges
- impossible to project sphere to plane without stretching
- visual quality changes based on user view direction
- need to consider best and worst areas of visual quality

### Equiangular cube map
- Great solution when uniformity is desired
- good candidate for offline/ unreliable bandwidth
- doesn't reach max resolution

### Directional projections
- places highest resolution within field of view
requires multiple versions for different areas of interest
requires low latency/ minimal buffering to switch fast

### Projection(s)
- Not necessarily the best option
- depends on content, view direction, bandwidth, device characteristics

### Adaptive streaming
- ...

## Spacial Audio with Dillon Cower @DCower
- ears are complex!
- Spacial audio represents sound space
- answers questions
   - where is sound coming from?
   - where am I?
- MUST location in space, capture the environment, immerse the listener.
- Latency causes a poor experience

### Finding a representation
- can't pre-render audio
- Surround sound
  - channels correspond to a speaker
  - build for front facing experiences
  - mostly horizontal speaker layouts

### Object based audio
- for each source:
  - mono audio + metadata
- audio engine for games basically
- great for post production and mastering
- predictable and consistent are great
- more sources need more data which isn't ideal for streaming

### Ambisonics
- full sphere spatial audio
- scene based representation
- First order ambisonics
  - mid side stereo technique
    - two mics to make a stereo image
    - 3D extension of mid-side stereo
    - form virtual microphones on the sphere

#### Spherical harmonics
- approximates a spherical function
- channels map directly to harmonics
- directivity patterns


#### First Order Ambisonics
- increases immersion
- room for improvement
- large margin of error
- solution is spherical harmonics

### Higher order ambisonics
- spherical harmonics are infinitely extendable
third order ambisonics has 16 channels of audio

#### Streaming Ambisonics
- goal is spacial audio for everyone
- audio tech not built for ambisonics
- first order ambisonics using quad layout
- Vorbis
  - multi channel Vorbis support is great
- not ideal because we want different bit distribution
- High fidelity audio steaming by Opus

#### Making spacial audio is hard
- lots of tools, lots of cycles
- **Jump** inspector app!!!
  - allows you to mix in real time and preview on your device in real time!

### Formats
- github.com/google/spatial-media/
