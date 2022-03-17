You can record animations in VTube Studio (`.motion3.json` files). These animations can then be used directly in your model or even re-imported into _Live2D Cubism_ to be used in the _Live2D Cubism Animator_ or the _Live2D Cubism Physics Editor_.

## Recording animations

Scroll down in the camera settings tab to "Record Live2D Animation". This is available on all platforms, including mobile. You can choose to record or exclude the physics output parameters as well. Keep in mind that if you save and play the recorded animation later in VTube Studio, physics parameters that are set by an animation will be ignored because they will be overwritten by the physics system.

If you deactivate **"Rec. unchanged params"**, VTube Studio will check for any parameters that did not change at all during recording and exclude them from the animation per default (you can turn them back on manually). This would for example exclude any parameters used as expression toggles that were not toggled during animation recording.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_1.png]]

After the recording is finished, you will be presented with the animation config screen. You can toggle individual parameters on and off to include/exclude them from the final animation. The slider lets you choose how much the animation for the selected parameter should be smoothed. The curve preview window will show the final animation curve for that parameter in red and the raw data in gray. The red dots mark the curve segment end points. If you plan to use the animation in the _Live2D Cubism Animator_, making sure that the curves look good and have a reasonable amount of points is important.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_2.png]]

After choosing a filename and saving, the animation will be saved as `<name>.motion3.json` in the same folder you've used for your other animations or next to the model file if you have no other animations.

## Re-importing Animations into Live2D

You can re-import animations (`.motion3.json` files created with VTube Studio) back into the _Live2D Cubism Animator_. To do that, start the _Animator_ for your model like you normally would (as in open the `.can3` file of your model or create one). Then, create a new animation

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_import_1.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_import_2.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/record_animation_import_3.png]]




