Two things should be implemented as part of this.

1) Saving/Loading item scenes using the UI.
2) Loading items using hotkeys.

# Glossary

* `Internal Item`: Item within the "Items" folder (GIF, PNG or animated PNG folder).
* `External Item`: Item outside the "Items folder (GIF, PNG or animated PNG folder).

# Basic item persistence between VTS sessions

* Items should be saved at their respective positions, including items attached to the Live2D model. 
* Meaning if VTS if quit with items in the scene, they will be automatically loaded again when VTS is started.
* This should only happen if `"Remember Scene"` is active in the VTube Studio config.
* This should work for external and internal items.
* This functionality is completely unrelated to item hotkeys and saving/loading item scenes.

# Saving Item Scenes

* Users should be able to save the current state of the items in the scene. The idea is that you can load internal and external items into the scene and then use a "save" functionality somewhere on the UI.
  * This UI has the option to include or exclude items attached to the model.
  * This UI shows a list of all items that will be saved.
* Each item is identified by its ID, which is its filename. No two items should have the same filename. For animated PNG folder items, the filename is the folder name.
* For each item, the saved properties are position, rotation and scale. For items attached to the model, the exact model attachment point is saved.
* Other saved properties: Scene order, smoothing value and "censored" state.
* If the scene is later loaded and a different model is active, items attached to the model won't be loaded. If this happens, failure to load the items will be logged appropriately.
* There will be a UI to list saved item scenes. This UI will also allow you to delete item scenes, show their contents or rename them.
* Item scenes will be saved in a folder called "Scenes". This folder will contain files called `"<scene-name-ascii>.scene.json"`.
* All items will be referenced as filenames in the "Items" folder. This means that `external items` will automatically have to be copied to the "Items" folder when a scene is saved with them included.
  * Thinking about it now, I think it makes sense to automatically save any external items in the "Items" folder the moment it is loaded into the scene.

# Loading item scenes.

The previously saved scenes can be loaded via a UI (or hotkeys, see below). The most complex point here is how to deal with items that appear in multiple scenes or how to deal with partially loaded/unloaded scenes. 

# Hotkeys

Unload all items
Quicksave/Quickload




# Item Quicksave and item Quickload






