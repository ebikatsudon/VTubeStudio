## Basic Setup

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_main.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_physics.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_autosetup.jpg" width="290" /> 
</p>

Once you have loaded a model, you will be able to access the model settings in the VTube Studio model config tab.

At the top, you can enter a name for your model. This name will be shown in the model selection bar.
Below that, you can see the name of the Live2D model file and the automatically created VTube Studio model file (VTS model).

You can choose an icon (.jpg or .png, click icon at top right to open file selection) and default idle animation (.motion3.json) for your model. You can choose from any file inside your model folder. 

You can also run the auto-setup for your VTube Studio model. This will set up your model based on standard Live2D parameter names and values. For more information about these parameters, please see: https://docs.live2d.com/cubism-editor-manual/standard-parametor-list/# 

If you change the parameter IDs or ranges, auto-setup will not be able to set up your model and you'll have to do it manually. Even if you use auto-setup, you may have to fine-tune your VTS model to fit your Live2D model.

## Model Movement

With the "Model Movement" settings, you can move the model left/right and closer/further away from the screen based on your head position. With the sliders, you can configure how much the model is moved.

## Physics Settings

Here, you can boost or reduce the effect of your Live2D physics setup. You can also activate “wind”, which will randomly apply a wind-like force to the physics system. This is experimental and may not look good depending on how your model is set up.

VTube Studio used to ignore the Live2D physics setting "Effectiveness". This has been fixed in a recent update. To turn on "Effectiveness", make sure the "Legacy Physics toggle is off.

## VTS Parameter Setup

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_params.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_param_in.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/model_settings_param_out.jpg" width="290" /> 
</p>

This is the most important part of your model settings. Here, you set up which face tracking parameters control which Live2D parameters.

The general idea is:

* You can freely map any INPUT parameter (face-tracking, mouse, etc.) to any OUTPUT parameter (Live2D parameter).
* How the values are mapped can be freely configured. For example, the input parameter MouthOpen is within the range [0, 1], with 0 being closed and 1 being all the way open. If your Live2D parameter (for example named ParamMouthOpen) has the range [-10, 10], you could map the ranges so (IN, 0) becomes (OUT, -10) and (IN, 1) becomes (OUT, 10). Or you map it any other way, there are no restrictions. 
* The red dot will show where the current value is placed within the input and output range.
* By activating "Limit Range", you can make sure the the input or output values never exceed the range you set for the input or output. This will also cause the value to stop smoothly when approaching the limits.
* Generally, it is recommended to only change the output range and leave the input range as is.
* More smoothing will make the movements less shaky but will introduce lag. Experiment with the smoothing values until you find something that works for each parameter. On iOS, you will most likely need very little smoothing.
* Auto-breath will fade the output parameter up and down in a breath-like motion. No input parameter is required when using this option. Any input will be ignored.
* Auto-blink will randomly reduce the parameter to zero. This can be combined with an input parameter, but none is necessary.
* As input parameter, you can choose from a list of available parameters. iOS supports more face tracking parameters than Android (see below).
* As output parameter, you can choose any Live2D parameter. Each output parameter can only be chosen once, as otherwise you would have multiple input parameters writing to the same output parameter.


---
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
If your model doesn’t move despite the Live2D parameter clearly moving in the VTS model config, the cause is most likely an expression, an animation or the physics system overwriting the value from the face tracking. This is explained in detail in the chapter:

[Interaction between Animations, Expressions, Face Tracking, Physics, etc.]()

---

