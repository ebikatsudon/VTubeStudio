## Creating Expressions

Expressions allow you to set Live2D parameters to certain values using hotkeys. Using expressions, you can for example trigger different facial expressions or costume changes.

Expressions can be set up directly inside of VTube Studio on the **"Hotkeys"** tab.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/expression_editor_1.png]]

From here, you can either **create a new expression**, **edit existing expressions** or **automatically create hotkeys for all expressions that don't have hotkeys yet**.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/expression_editor_2.png]]

When editing expressions or creating new ones, the following window is shown. Select/Deselect the Live2D parameters that you want to be part of the expression. You can't use physics output parameters in expressions because their value is overwritten by the physics system.

Saving a new expression will create an `.exp3.json` file in your model's directory. If you already have expressions in a separate folder for your model, VTube Studio will use that folder for new expressions.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/expression_editor_3.png]]

_Note:_ Alternatively, expressions can be created using the **Live2D Cubism Viewer**. You can download it for free as part of the Live2D Cubism Editor: https://www.live2d.com/en/download/ 

## Using Expressions

To use the expressions in VTube Studio:

1. Create a new hotkey inside of VTube Studio as explained in the chapters about hotkeys.
2. Use the hotkey type "Set/Unset Expression"
3. Select your expression file from the list. If you can’t find it there, make sure the _.exp3.json_ file is in the same folder as your VTS model file or in a subfolder of it.
4. Your hotkey is now fully set up. You can use either your keyboard or the on-screen buttons to activate and deactivate it. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
When multiple hotkeys modify the same Live2D parameter, the value of the last activated hotkey is used. When you then deactivate the "last" hotkey, the value is returned to the value of the "previous" hotkey. When all hotkeys that modify a certain Live2D parameter are deactivated, that parameter is returned to the value from the animation, the value from face tracking or the default value. More on this in the chapter:


[Interaction between Animations, Expressions, Face Tracking, Physics, etc.](https://github.com/DenchiSoft/VTubeStudio/wiki/Interaction-between-Animations%2C-Tracking%2C-Physics%2C-etc.)
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]