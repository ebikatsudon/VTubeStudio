VTube Studio can take the average color from your screen (Windows/MacOS) or any window (Windows only) and overlay it over your model, including attached items. This makes it seem like your model is "in the game/video" in your OBS/Streamlabs scene. Inspired by [this post by @Virtual_Graves](https://twitter.com/Virtual_Graves/status/1434154401707397120).

There may be a small delay (~100 ms) for the lighting to be calculated. You can add a source render delay to your other capture in OBS to make up for that.

## Display Light Overlay Basic Setup

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_lighting_overlay.png|alt="VTube Studio Display Light Overlay"]]

There are the following options:
* **Display**
  * The activated display.
* **Brightness**
  * Base brightness level. It's best to keep this low.
* **Overlay**
  * Color overlay multiplier. The higher you set this, the more the color overlay will be shown. If it's too high, your model might be very bright when there are bright colors on screen.
* **Smoothing**
  * Smoothing for the color values. 3-4 is a good value.
* **Include Items**
  * Whether or not items should also be tinted.

The colored circles below the screen preview show the respective average color calculated for the left, middle and right screen part. You can click them to include/exclude them from the average color calculation. That way, you could tint your model only using the color of a part of your screen.

## Display Light Overlay Hotkeys

You can also control this via hotkeys. Just create a hotkey with the type **"Screen Overlay"** and click **"Record Settings"** to record the current display color overlay settings into a hotkey.

