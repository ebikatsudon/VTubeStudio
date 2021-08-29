You can import your own props ("items" or "assets") directly into the scene and even attach them to your Live2D model.

Items are read from the **"Items" folder next to your "Live2DModels" folder**. VTube Studio comes with a few items included, but you can add your own by putting PNGs into that folder.

If you put a **folder** into the **"Items" folder**, this folder will be considered to contain the frames for an **Animated Item**. PNGs you put into that folder will be read in alphabetical order and combined into an animation that can be loaded like a regular item in VTube Studio. Keep in mind that items with many frames may take up to a couple seconds to load.

FPS for the animated item can be set freely between 0 and 60 and once set will be remembered when you load the item again.

It’s recommended but not required to keep frames of an animated item at the same size. The “hitbox” (clickable part of the item) will be based on the first frame of the animated item.
