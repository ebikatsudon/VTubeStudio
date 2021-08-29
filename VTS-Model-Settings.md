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

If you change the parameter IDs or ranges, auto-setup will not be able to set up your model and you’ll have to do it manually. Even if you use auto-setup, you may have to fine-tune your VTS model to fit your Live2D model.

## Model Movement

With the "Model Movement" settings, you can move the model left/right and closer/further away from the screen based on your head position. With the sliders, you can configure how much the model is moved.

## Physics Settings

Here, you can boost or reduce the effect of your Live2D physics setup. You can also activate “wind”, which will randomly apply a wind-like force to the physics system. This is experimental and may not look good depending on how your model is set up.

The "Legacy Physics" toggle 



