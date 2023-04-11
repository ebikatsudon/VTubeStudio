**Note:** For general information about Items/Assets (custom JPG or PNG images or GIFs you can attach to your model), see the page ["Item System"](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System).

## Item Scenes

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_toggle.gif]]

You can spawn items (or unload them) via Hotkeys.

This works for items that are attached to the model and items that aren't.

To do this, you first have to create an **"Item Scene"**, which is a collection of items that are turned on/off together. If you just want to turn one item on and off, that _Item Scene_ can just contain that one item.

To create an _Item Scene_, first load all the items you'd like to include and position them however you want them to be saved, including attaching them to the currently loaded model if you want. Then open this menu and create a new _Item Scene_.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_create.png]]

This will open a new window that lets you set up the _Item Scene_ based on the currently loaded items. Click items to remove them from the scene (red) or include them again (blue). The info button ("i") shows information about the respective item, such as the position, rotation, etc.

The number next to the item thumbnail image is the order of the item in the _Item Scene_. When the _Item Scene_ is loaded, this order will be used when spawning items. When the order is already taken, the next higher order will be used until the scene is full.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_setup.png]]

You have to give your _Item Scene_ a name, which will be used to identify the scene. No duplicate names are allowed. Additionally, you can also add a **"Item Scene Group"** (just called **"Group"** from here on, more on that later). If the item is attached to a model, this is also shown in the list as you can see.

After creating the _Item Scene_, you can set up a hotkey that toggles that scene. You can set a fade in/out time for the _Item Scene_ (can also be instant) and optionally set the _Item Scene_ to deactivate X seconds after activating it (up to one hour). The idea here is that you could have a Twitch redeem that turns on a hat, glasses, etc. for a certain amount of time. 

In this example, the _Item Scene_ **"Beard and Glasses** will be loaded/unloaded when the hotkey is activated. Items that have been loaded as part of an _Item Scene_ can be used like normal items. You can for example delete them from the scene by dragging them out of the window or drop them on the trash can. When pressing the hotkey again and there is still at least one item from that _Item Scene_ loaded, all remaining items from that _Item Scene_ will be unloaded.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_hotkey_setup.png]]

## Item Scene Groups

You can set up as many _Item Scenes_ as you want and also load them at the same time. Sometimes there are situations where you want one _Item Scene_ to unload automatically if you load a different one, for example when you have many different hats for your model and only want one to be active at a time. This is what _Item Scene Groups_ are used for. 

**Example:** If an _Item Scenes_ that has the _Group_ **\<A\>** is activated, there could be other items already loaded that were loaded by another _Item Scene_ that has the _Group_ **\<A\>**. These items would then be automatically unloaded.

## Modifying Item Scenes

You can modify _Item Scenes_ after creating them. This means adding items, removing items or modifying them (for example pinning them to a different position on the model). Just open the _Item Scene_ in the _Item Scene_ selection window and save it again. To modify existing items in the scene, you first have to load that scene via a hotkey, then do your changes (for example moving or pinning the item somewhere else), then open the _Item Scene_ selection window and then save.

The only thing you cannot change is the scene name. If you want to change that, you'll have to delete and recreate the _Item Scene_ from scratch.

## Can I have one Item Scene with items pinned to different models?

Yes, that's possible. Just load the model you want to add items to the _Item Scene_ for and then add those items to the existing _Item Scene_ which already contains items pinned to different models.

When an _Item Scene_ is loaded using a hotkey and it contains pinned items not intended for the currently loaded model, those items are skipped and will not be loaded.

## Can I use have YouTube/Twitch redeems or chat commands that let viewers spawn items?

Yes, that's possible! Just create an item hotkey as described above and then use a [plugin](https://github.com/DenchiSoft/VTubeStudio/wiki/Plugins) to let viewers trigger it. You could even set the item scene hotkey to auto-deactivate after a few seconds/minutes.

For more info, check out the plugins page: https://github.com/DenchiSoft/VTubeStudio/wiki/Plugins

## Does loading Item Scenes cause lag?

Only the first time the _Item Scene_ is loaded after starting VTube Studio. After that, the textures will be cached in memory so loading should be instant.

## My pinned items don't move correctly! What gives? (ArtMesh Pin Exclusion)

The item might be pinning to the wrong ArtMesh. Items generally pin to the topmost ArtMesh that's not set as "invisible" (0% opacity) or "deactivated" in your Live2D model. If you for example have some big blush overlay layer in front of your face, items may pin to that and move in unexpected ways.

Open the logs when dropping items on your model to see the ID of the ArtMesh your item is pinning to.

There is a menu that lets you exclude ArtMeshes from having items pinned to them:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_model_customize.png]]

### Alternative: Exclude ArtMeshes from pinning directly in your Live2D model 

If you're making a Live2D model and have layers in the model that you already know no item should pin to, you can exclude them directly in the model by marking the ArtMeshes. There are two options:

* **[NOT GOOD]** Have `vts_ignore_raycast` as part of the ArtMesh ID. VTS does a contains-match, so it can be anywhere in the ID.
* **[BETTER]** Have `vts_ignore_raycast` somewhere in the UserData field for that ArtMesh. When you export your model, make sure you have `Export UserData file (userdata3.json)` checked. This will give you a `<modelname>.userdata3.json` file that contains the IDs and UserData-tags of tagged ArtMeshes. This is better because it creates an additional JSON file that you can add/remove/modify anytime you want.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_ignore_raycast_a.png]]


