You can copy the VTube Studio configuration from one model to another. This can be useful if you have multiple models with similar Live2D parameters.

You can access this menu from within the **"Auto Setup"** menu. First, load the **model you want to copy from**. Then go to **"Auto Setup"** and select **"Copy setup from other model"**. This will show a list of all models in VTube Studio and you can **select one to copy from**.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/copy_setup_from_model_1.png]]

## Things you can copy

You can copy the following things between models:

* **[Basic settings]** - This copies the basic model settings, such as the "Movement Config" and idle animation names.
* **[Physics/Wind settings]** - This copies all model settings related to physics and wind.
* **[Parameter setup]** - This copies all parameter settings, so which tracking (INPUT) parameters are mapped to which Live2D (OUTPUT) parameters.
* **[Hotkeys]** - This copies all settings related to hotkeys.
* **[Expression files]** - This copies all expression files (`.exp3.json`) from the model.
* **[Animation files]** - This copies all animation files (`.motion3.json`) from the model.
* **[Model icon]** - This copies the model icon file.
* **[ArtMesh settings]** - This copies over all per-ArtMesh data, such as item pinning exclusions, lighting system customization and more.


Rename missing parameters




 Make sure the destination model has the same Live2D parameters as the source model, otherwise some parameter settings may not work as expected. If that happens, the missing parameters will be marked in red.