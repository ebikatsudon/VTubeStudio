**Note:** This page uses the words _"item"_, _"asset"_ and _"prop"_. They refer to the same thing. 

For information about items/assets/props in _VTube Studio_ in general, check out [this other page](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System).

## What are Live2D Items?

In addition to [normal PNG, JPG and animated assets](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System) (GIF, etc.), VTube Studio now supports adding Live2D-props into the scene. You can also attach them to your model. With this, you can create props that react to face-tracking, have physics and can even have their own hotkeys to trigger expressions and animations in the prop Live2D models.

You could for example have animated hats, guns that aim depending on your face angle and shoot when you click with your mouse or glasses that properly rotate with your head. Live2D props also support physics.

<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/pudding_head_gif.gif" />
</p>

When set up correctly, their physics setup will also react when they’re attached to your model and your model moves them.

## How do I load/use Live2D Items?

You load them like regular items. You can also filter the item list to only show Live2D items (see image below). Options like **"flip"** and **"item order"** are available for Live2D items as well.

[Just like normal items](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System), Live2D items are read from the "Items" folder. Any folder in the "Items" folder that contains a **valid VTube Studio model** will be considered a Live2D item, so you can copy any model you want in there and it show up in the items list.

When you flip a Live2D item, its X/Z axes will be inverted. That way, items like animal ears can easily be loaded into the scene twice, with one of them flipped, and they will rotate correctly.

To flip an item that’s been loaded into the scene already, you can **[CTRL] + Click** it. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_items_select.png]]

## How can I configure/fine-tune my Live2D Items? For example, the head rotation range (X/Y-angle) doesn't fit my model. What do I do?

Sometimes, items were made with models in mind that rotate more/less than your own model in the X/Y head direction. This can be important for assets like glasses.

This can easily be fixed by selecting the item you want to configure and pressing the **“Configure/Finetune Live2D Item”**. From there, you can set multipliers for the “ParamAngleX/Y/Z” Live2D output parameters the Live2D item model uses. You can also finetune the smoothing values used by the respective parameters of the Live2D item here.

The **“Return to default when not pinned”** option will make the item return the “ParamAngleX/Y/Z”  parameter values to their default when the item is not pinned. That way, you could for example prevent glasses from rotating/deforming when they’re not actually pinned to your model. 

If you activate **“Use normal hotkey triggers”**, the normal key combinations set to trigger hotkeys in the item’s VTS model can be used to actually trigger the hotkeys when the item is loaded.

Finally, you can adjust the **“Dragging Physics”**. Dragging physics will push the physics inputs left/right when the item is being dragged or is moving because it is attached to the main model. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/configure_item_live2d.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_items_adjust_params_with_button.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Dragging physics can also be used for normal VTube Studio models. You can set that up in their physics settings tab.
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## How do I trigger Hotkeys in my Live2D Items?

### Option A: _Using normal hotkeys_

If you have activated **"Use normal hotkey triggers"** for the Live2D item, you can use the normal keyboard trigger keys set up in the VTube Studio model of the item to trigger them, as long as they are related to expressions or animations.

### Option B: _Using "Item Actions" set up in your main model_

You can trigger hotkeys that have been set up in the Live2D item via hotkeys of your main model. Only hotkeys that meet the following requirements can be triggered this way:

1. Hotkey must be of type **"Expression"**, **"Remove Expressions"** or **"Animation (idle/normal)"**
2. Hotkey must have a name set. The name cannot be empty.

You can set up a hotkey in your model of type **"Live2D Item Action"**:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_items_action_hotkey_1.png]]

When you set up a hotkey of that type, it will show you a list of all hotkeys in all your Live2D items. So when you trigger that hotkey, it will trigger the selected hotkey in the selected item (but only if it is loaded).

If you have multiple instances loaded of the same Live2D item, this will trigger the hotkey in all of them.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Like normal items, Live2D items can be loaded/unloaded via **"Item Scene" hotkeys**.
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_items_action_hotkey_2.png]]

Alternatively, you can also select the options **"Hotkey 1/2/3/4 of last clicked Live2D Item"**. Using this hotkey lets you trigger the X-th (supported) hotkey in the last clicked loaded/clicked Live2D item.

## Can I change the color of some parts of the Live2D Items (for example skin color)?

For some items, you may want to change the colors of certain parts. For example, you could change the skin color of assets that contain hands to match the skin color of your model. Other uses include re-coloring drinks, glasses and much more.

To that, load the Live2D item you want to re-color using the **"Configure/Finetune Live2D Item"** button. After pressing **"Save"**, you will see this prompt:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_item_recolor_yes_no.png]]

From there, you can now configure a "multiply" and "screen" color per ArtMesh. When applying these settings, they will be saved into your model file so whenever you next load that item, it will have your color settings applied (including when you load the Live2D Item via Item Hotkeys).

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Setting "Screen" and "Multiply" overlays via normal Live2D parameters (_Live2D Cubism 4.2_ and up) will no longer work for the ArtMeshes you re-color using this menu.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_item_recolor.png]]

