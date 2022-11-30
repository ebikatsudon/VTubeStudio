### Recording Animations

You can record animations in VTube Studio based on tracking. For more info, check the ["Record Animation"](https://github.com/DenchiSoft/VTubeStudio/wiki/Record-Animations) page.

However, normally you would create animations in the **Live2D Cubism Animator**.

### Loading Animations

Animations can be created with the **Animator** in the **Live2D Cubism Editor**. Once your animation is done, select **File → Export for Runtime → Export motion file**.


This will give you _.motion3.json_ files (Live2D animation files) that can be read by VTube Studio. Put them in the same folder as your VTS model or a subfolder.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/export_motion.png]]

These animations can be used as looping background idle animation or one-shot animation.

In VTube Studio, you can also use various settings for animation playback, such as:
* Ending animation after X seconds.
* Holding animation on last frame
* ...

