Two things should be implemented as part of this.

1) Saving/Loading item scenes using the UI.
2) Loading items using hotkeys.

# Glossary

* `Internal Item`: Item within the "Items" folder (GIF, PNG or animated PNG folder).
* `External Item`: Item outside the "Items folder (GIF, PNG or animated PNG folder).

# Basic item persistence

* Items should be saved at their respective positions, including items attached to the Live2D model. 
* Meaning if VTS if quit with items in the scene, they will be automatically loaded again when VTS is started.
* This should only happen if `"Remember Scene"` is active in the VTube Studio config.
* This should work for external and internal items.
* This functionality is completely unrelated to 



