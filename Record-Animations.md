You can record animations in VTube Studio (`.motion3.json` files). These animations can then be used directly in your model or even re-imported into _Live2D Cubism_ to be used in the _Live2D Cubism Animator_ or the _Live2D Cubism Physics Editor_.

## Recording animations

Scroll down in the camera settings tab to "Record Live2D Animation". This is available on all platforms, including mobile. You can choose to record or exclude the physics output parameters as well. Keep in mind that if you save and play the recorded animation later in VTube Studio, physics parameters that are set by an animation will be ignored because they will be overwritten by the physics system.

If you deactivate **"Rec. unchanged params"**, VTube Studio will check for any parameters that did not change at all during recording and exclude them from the animation per default (you can turn them back on manually). This would for example exclude any parameters used as expression toggles that were not toggled during animation recording.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_1.png]]

After the recording is finished, you will be presented with the animation config screen.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_2.png]]