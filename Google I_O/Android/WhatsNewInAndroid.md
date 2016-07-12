# Session: What's new in Android
## Wednesday May 18, 2016

# User Facing Features
## Constraint Layout
- Compatible back to gingerbread.
- Friday 9 am. Constrait layouts
- Alpha 1 in AS 2.2 preview

## MultiWindow Split screen
- android: resizableActivity-["true" | false ]
- Activity.isInMultiWindowMode()
- Activity,onMultiWindowModeChanged
- more...

## Picture in Picture mode
- android:SupportsPictureinPicture

## Drag and drop
- android.view.DragAndDropPermissions
- Activity.requestDragAndDropPermissions
- View.startDragAndDrop()
- ...
- View.cancelDragAndDrop()
- ...

## Notifications
- Thursday 9am
- New templates!
- Bundled Notifications
- Direct reply

## Quick Settings
- reorder-able
- 5 quicker quick Settings
- Create your own tiles
  - android.service.quicksettings.TileService
  - android.service.quicksettings.Tile
  - put the service in the manifest

## Display Size
- augment and change font Size
- Display size changes the DPI of the device at runtime
- changes all UI not just text
- .85 -> 1.45
- avoid px
- ensure your app works well on sw320dp!

## MultiLocale
- user can select multiple languages and order them
- added new languages, variants

## Doze
- no network Activity
- helps with battery a lot
- screen off, on battery, not stationary
- restricts network...

## Project Svelte
- battery and memory optimization Wednesday at 5
- deprecated
  - ConenctivityManager.CONNECTIVITY_ACTION
  - Camera.ACTION_NEW_VIDEO
  - Camera.ACTION_NEW_PICTURE
- new approach is JobScheduler
  - JobScheduler.Builder.addTriggerContentUri();

## Data Saver
- Tell specific apps if they can use data or not in System Settings
- getSystemService(Content.CONNECTIVITY_SERIVCE)
- ConeectivitiyManager.is active or something

## Direct Boot
- improves startup time
- Some App functionality after unexpected reboot
- Thursday 9am

### Scoped Directory Access
- permission to just a file in a folder

### Android for Work
- Thursday 2pm: Apps at work
- Work mode aka not work mode
- Work Challenge

# Developer Features!
## Runtime
- faster interpreter
- JIT
  - faster install times
  - less space consumed on device
  - Apps use partial AOT
    - only for hotspots
    - Evolution of ART on Friday
- New runtime libraries
  - ICU4J
  - FunctionalInterface
  - java.util.function
  - ...

## Java 8 Features
- Lambdas
  - Compatible to gingerbread
  - implemented using anonymous classes
- need to add to gradle

## Default and Static interface methods
- not backwards Compatible
- use for adapter pattern

## Repeating Annotations
- not backwards Compatible

## Java Audio Latency
- previous releases reduces native latency
- lower latency AudioTrack (40-70ms reduction)
- AudioAttributes

## Renderscript
- Single source
  - many kernels in a single file
  - Allocation....

## OpenGL 3.2
- Android extension pack
- advanced blending
- geometry shaders
- ASTC (LDR)
- Image atomics
- Floating point frame buffers

## Vulkan
- Low level low overhead cross platform 3D API
- Asynchronous/multi threaded command generation
- no error checking
- object based api, no global state
- offline shaders cpompilation
- intermediate shader binary format

## ADB Shell
- returns remote process exit status
- pass through stdin
- handles window size and terminal tyope
- improved command line tools
- improved performance (push,pull)

## NDK
- Clang 3.8
- GCC 4.9
- Switch to Clang GCC is deprecated

## VR VR VR!!!
- Activity.setVrModeEnabled(boolean, ComponentName)

## Support Library
- 23.2
  - Night mode
  - bottom sheets UI
  - VectorDrawable / AnimatedVectorDrawable
  - RecyclerView AutoMeasure
- 23.1
  - RecyclerView improvements
- The Future
  - Whats new in the support library today at 4pm

## Other UI Goodies
- VectorDrawable performance improved 20-90% loading and rendering
- FloatProperty / IntProperty

## Instant Apps
- Build inside studio
- different artifact
