Expressions are created using the **Live2D Cubism Viewer**. You can download it for free as part of the Live2D Cubism Editor: https://www.live2d.com/en/download/ 

Expressions allow you to set Live2D parameters to certain values using hotkeys. Using expressions, you can for example trigger different facial expressions or costume changes.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/expressions.png]]



## Alternative (outdated): Create expressions with the Live2D Cubism Viewer

To create expressions, first load your model into the Live2D Cubism Viewer by dragging in the _.model3.json_ file. Your model should now be open and ready to edit.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/akari_expression_editor.png]]

To create a new expression, you can now do the following:

1. Add a new expression using **File → Add → Expression**
2. Make sure **Animation → Apply Expression** is activated.
3. There should now be a folder called "Expressions" in the navigation window. Open it and click your newly created _.exp3.json_ file.
4. Create your expression by adjusting the sliders and checkboxes for the parameters you want to be part of the expression.
5. Fade-times are ignored by VTube Studio in the current version. Instead, a default fade-time is used. Alternatively, you can set a fade-time inside of VTube Studio.
6. You can also right-click a parameter and set it to "Multiply". This is not yet supported by VTube Studio and may result in your expressions not working. Please leave it at "Additive".
7. To save the expression, right-click your _.exp3.json_ file and select "Save". Save it somewhere next to your VTS/Live2D model or in any subfolder of that folder so VTS can find it when your model is loaded.

To set up the expressions in VTube Studio:

1. Create a new hotkey inside of VTube Studio as explained in the chapters about hotkeys.
2. Use the hotkey type "Set/Unset Expression"
3. Select your newly created expression from the list. If you can’t find it there, make sure the _.exp3.json_ file is in the same folder as your VTS model file or in a subfolder of it.
4. Your hotkey is now fully set up. You can use either your keyboard or the on-screen buttons to activate and deactivate it. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
When multiple hotkeys modify the same Live2D parameter, the value of the last activated hotkey is used. When you then deactivate the "last" hotkey, the value is returned to the value of the "previous" hotkey. When all hotkeys that modify a certain Live2D parameter are deactivated, that parameter is returned to the value from the animation, the value from face tracking or the default value. More on this in the chapter:


[Interaction between Animations, Expressions, Face Tracking, Physics, etc.](https://github.com/DenchiSoft/VTubeStudio/wiki/Interaction-between-Animations%2C-Tracking%2C-Physics%2C-etc.)
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]