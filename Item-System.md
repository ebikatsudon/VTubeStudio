## Loading Items into the Scene

**Note:** If you want to learn how to use hotkeys to spawn items, check out [this](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-Scenes-and-Item-Hotkeys) page.

You can import your own props ("items" or "assets") directly into the scene and even attach them to your Live2D model.

Items are read from the **"Items" folder next to your "Live2DModels" folder**. VTube Studio comes with a few items included, but you can add your own by putting PNGs into that folder.

If you put a **folder** into the **"Items" folder**, this folder will be considered to contain the frames for an **Animated Item**. PNGs you put into that folder will be read in alphabetical order and combined into an animation that can be loaded like a regular item in VTube Studio. Keep in mind that items with many frames may take up to a couple seconds to load.

You can also add GIFs as animated items.

FPS for the animated item can be set freely between 0 and 60 and once set will be remembered when you load the item again.

It's recommended but not required to keep frames of an animated item at the same size. The "hitbox" (clickable part of the item) will be based on the first frame of the animated item.


<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_selection_list.jpg" width="394" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_setup.jpg" width="394" /> 
</p>

First, choose the item you'd like to add. Then choose an order. Items with a higher order are in front of items with a lower order. The Live2D model itself is at order 0, so you can also place items behind it.

If you want the item to be able to attach to the Live2D model, make sure to select **"Pin item to Live2D model"**.

There is an experimental **"Censor"** option that applies a mosaic censor effect to the item. There is also a **"Mirror"** option that reflects the item.

By using the **"Smoothing"** slider, you can make the item follow your model more smoothly/loosely. Smoothing for an item will only be active when the item is locked (double-click the item after attaching it to the model).

If the item is **animated** (must be multiple PNGs in a folder in the "Items" folder), you can set the FPS here. It's generally recommended to keep item FPS under 45. You can put any floating-point number here, so even something like 3,7 FPS is valid.

Alternatively, you can also use GIFs as animated items, but it is recommended to use PNG sequences as described above to get the best quality (GIFs can be a bit grainy).


<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_main.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_lock.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_delete.jpg" width="290" /> 
</p>

Once the item is in the scene, you can move/scale/rotate it with the same controls as for the model on PC/Mac and iOS/Android. To attach an item to the model, just drop it on there.


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
The item will be attached to the uppermost ArtMesh in your model at the position where you drop the item. The point of attachment will be the **CENTER OF THE ITEM IMAGE**. This can make it a bit tricky sometimes to attach the item to the correct ArtMesh, so you may need to play around a little bit to make it work properly.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

Once your item is at the correct position, **you can double-tap (double-click) it to lock the position**. That way, you can no longer move, scale or rotate the item until it is unlocked again. If the item is attached to your model, it will still move according to the model movement.

If you move, scale or rotate the Live2D model itself, any locked items attached to the model will also move, scale and rotate with it as you would expect.

**To unlock locked items**, choose the option from the main menu (see arrow in second image). By pressing that button once more, all items will be locked again.

**To delete items from the scene**, simply drag them over the trash can icon in the bottom right. It will only appear if you drag an item near it. You can also drag and drop items off-screen, that will also delete them from the scene.

You can `[Ctrl] + Click` items to flip them (only if not locked).

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Most of the free included items/props have been provided by **@catboymech** and **@7MDigital** on Twitter. They have many other great VTuber assets as well, so please make sure to follow and thank them!! \<3

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## Item Drag & Drop

On Windows and macOS you can also directly drag items into the VTube Studio window. You can drag them from anywhere on your PC or Mac (any folder, desktop, etc.) onto the VTS window and they will spawn at the center of the scene. They will be set to 0 smoothing and to track the model, so you can attach them afterwards. This allows you to add items to the scene without opening the UI mid-stream.

You can drag in PNGs, JPGs, GIFs and folders containing PNG animation frames, which will be imported as animations. On Windows, you can also drag in multiple files at the same time. Items added later will be placed in front of items added earlier. The limit for the maximum number of items still applies.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/drag_and_drop.png]]





