VTube Studio can take the average color from your screen (Windows/MacOS) or any window (Windows only) and overlay it over your model, including attached items. This makes it seem like your model is "in the game/video" in your OBS/Streamlabs scene. Inspired by [this post by @Virtual_Graves](https://twitter.com/Virtual_Graves/status/1434154401707397120).

There may be a small delay (~100 ms) for the lighting to be calculated. You can add a source render delay to your other capture in OBS to make up for that.

**IMPORTANT: If this does not work, try starting VTube Studio as admin. On macOS, you need a recent OS version for this feature to work, most likely "Big Sur" or newer.**

## Display Light Overlay Basic Setup

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_lighting_overlay.png|alt="VTube Studio Display Light Overlay"]]

There are the following options:
* **Display**
  * The activated display. On Windows, you can also select a specific window here using the "Window" button.
* **Brightness**
  * Base brightness level. It's best to keep this low.
* **Overlay**
  * Color overlay multiplier. The higher you set this, the more the color overlay will be shown. If it's too high, your model might be very bright when there are bright colors on screen.
* **Smoothing**
  * Smoothing for the color values. 3-4 is a good value.
* **Include Items**
  * Whether or not items should also be tinted.

The colored circles below the screen preview show the respective average color calculated for the left, middle and right screen part. You can click them to include/exclude them from the average color calculation. That way, you could tint your model only using the color of a part of your screen.

## Window Capture

Using one specific window as color overlay source is only available on Windows (no macOS). When you click the "Window" button, it will show you a list of windows and displays that you can select from. Anything you select here will be captured **(if it's not minimized)** but, unlike the full display capture, will have a yellow border around it that currently cannot be removed (restriction of Windows WinRT capture).

You can also select "current window" from that list. If you select this and then create a hotkey based on that setting, activating the hotkey will switch the capture to the window you have currently focused.

## Display Light Overlay Hotkeys

You can also control this via hotkeys. Just create a hotkey with the type **"Screen Overlay"** and click **"Record Settings"** to record the current display color overlay settings into a hotkey.

For window captures, it will look for the exact window name of the window that was captured when the hotkey was recorded (unless it was set to "current window").

