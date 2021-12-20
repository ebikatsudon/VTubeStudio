**Note:** For general information about Items/Assets (custom JPG or PNG images or GIFs you can attach to your model), see the page ["Item System"](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System).

## Item Scenes

You can spawn items (or unload them) via Hotkeys.

This works for items that are attached to the model and items that aren't.

To do this, you first have to create an **"Item Scene"**, which is a collection of items that are turned on/off together. If you just want to turn one item on and off, that _Item Scene_ can just contain that one item.

To create an _Item Scene_, first load all the items you'd like to include and position them however you want them to be saved, including attaching them to the currently loaded model if you want. Then open this menu and create a new _Item Scene_.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_create.png]]

This will open a new window that lets you set up the _Item Scene_ based on the currently loaded items. Click items to remove them from the scene (red) or include them again (blue). The info button ("i") shows information about the respective item, such as the position, rotation, etc.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_setup.png]]

You have to give your _Item Scene_ a name, which will be used to identify the scene. No duplicate names are allowed. Additionally, you can also add a **"Item Scene Group"** (just called **"Group"** from here on, more on that later). If the item is attached to a model, this is also shown in the list as you can see.

After creating the _Item Scene_, you can set up a hotkey that toggles that scene. You can set a fade in/out time for the _Item Scene_ (can also be instant) and optionally set the _Item Scene_ to deactivate X seconds after activating it (up to one hour). The idea here is that you could have a Twitch redeem that turns on a hat, glasses, etc. for a certain amount of time. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/item_scene_hotkey_setup.png]]







