You can copy the VTube Studio configuration from one model to another. This can be useful if you have multiple models with similar Live2D parameters.

You can access this menu from within the **"Auto Setup"** menu. First, load the **model you want to copy from**. Then go to **"Auto Setup"** and select **"Copy setup from other model"**. This will show a list of all models in VTube Studio and you can **select one to copy from**.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/copy_setup_from_model_1.png]]

## Things you can copy

You can copy the following things between models:

* **[Basic settings]**
  * This copies the basic model settings, such as the "Movement Config" and idle animation names.
* **[Physics/Wind settings]**
  * This copies all model settings related to physics and wind.
* **[Parameter setup]**
  * This copies all parameter settings, so which tracking (INPUT) parameters are mapped to which Live2D (OUTPUT) parameters.
* **[Hotkeys]**
  * This copies all settings related to hotkeys.
* **[Expression files]**
  * This copies all expression files (`.exp3.json`) from the model.
* **[Animation files]**
  * This copies all animation files (`.motion3.json`) from the model.
* **[Model icon]**
  * This copies the model icon file.
* **[ArtMesh settings]**
  * This copies over all per-ArtMesh data, such as item pinning exclusions, lighting system customization and more.

If the expression and animation files for the target model (the one being copied to) are in a subfolder, VTube Studio will automatically copy any new animation files into that folder as well.

## What if the models have different Live2D parameters?

The model setup, animations and expressions will only work properly if the source model (model being copied from) and the target model (model being copied to) have the same Live2D parameters. Otherwise, these parameters will be missing in the model setup (they will be marked red in the target model) and animations/expressions will ignore these parameters.

If you activate **[Rename missing parameters]**, VTube Studio will automatically attempt to find missing Live2D parameters by checking different parameter capitalizations and parameter ID styles. For example, if the source model uses the old parameter ID style (ex. `PARAM_ANGLE_X`) and the target model uses the new parameter ID style (ex. `ParamAngleX`), the parameters will be automatically corrected in the model setup, expressions and animations after copying them over.

For more info about default Live2D parameter IDs, check this page: https://docs.live2d.com/cubism-editor-manual/standard-parametor-list/?locale=en_us


