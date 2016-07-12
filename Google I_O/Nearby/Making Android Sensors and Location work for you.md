# Making Android sensors and location work for you
## Wednesday May 18, 2016
Speakers:
- Steve Malkos
- David Christie
- Ashutosh Joshi

# Building Aware Experiences
- Sensors
- Location
- Android Sensor Hub

### What does it take to build high quality apps?
- User experience
- Algorithms
- Sensors

### Awareness Pillars
1. Coverage
- Accuracy
  - under 5 meters all the time is the goal
- Latency
- Power

## Android Sensors
- Android N supports 32 sensor types
- N API for Augmented Reality: 6DOF
- N API for Fitness and Wear: Heart Rate Variability
- N API for Simple Motion: Motion detector
- N API for Screen Orientation: Screen Orientation...
- N API for External Sensors: Dynamic Sensor Discovery

## We Push the Ecosystem forward
- standards
- Google devices
- collaborate with partners

### Standards are defined in CDD
- These standards are enforced with CTS
  - all apps must pass these tests
- Google devices allows us to keep pushing forward
  - to make everyone else make better devices by making competition in the space

### We share our tech for our OEM partners
git clone android.googlesource.com/device/google/contexthub

### Hardware Triggering
- Geofences
- Sig Motion

## Use the highest Level APIs you can
- allows google to make android better for apps automatically
  - examples: batching, screen orientation

### Hifi Sensors guarantee quality
  - low latency

#### Check for HiFi sensors
  if(packingManager.hasSystemFeature(PackageManager.FEATURE_HIFI_SENSORS)) {
    .. do stuff
  }

## Fused Location Processor
  - Combines GPS, wifi cell, accelerometer, Gyro, and magnetometer
  - GPS
    - Coverage: outdoors
    - Accuracy: Great
    - Power: poor
  - WiFi
    - Coverage: indoors
    - Accuracy:
    - Power:
  - Cell
    - Coverage:
    - Accuracy:
    - Power: great

## Sensor Fusion Improvements
- Improve Power and Accuracy

## Location Batching

RequestLocationBatching.Java
LocationRequest req = new LocationRequest();
req.setPriority9LocationRequest.PRIORITY_BALANCED_POWER_ACCURACY);
...

## Geofencing
- Allows app response to locations of interest
- Fused location and activity recognition

Look online for *RequestGeofencing.java*

- Building Contextual Experiences
- Sensors
- Location
- Android Sensor Hub

## Android Sensor Hub
- Use all sensors to get better context and location
- Augment human memory and knowledge
- The hub
  - Runtime, algorithms, and processor
  - Low power always on processing
  - Launched in marshmallow
  - Built into the 5X and 6P


- What did we build into Marshmallow?
  - dude skipped the slide...


- Whats in the hub?
  - Everything is in sensors.h
  - Significant motion
  - activity recognition
  - Double Twitch?!

### Huge Power Saving with Activity Recognition

- What are we currently building?
- GPS Pseudoranges
- Personalized Activity
- Android Sensor Hub
  - Download Code
  - Connectivity
    - GPS
    - WIFI
    - Cell

## Future/ Closing Thoughts
- 3 Key Questions
  1. Where is the user? Location
  2. What is the user doing? Activity
  3. What is near the user? Nearby


- Bringing always on Location and Personalized contacts

developers.google.com/locations-awareness

goo.gl/d9bxdr
