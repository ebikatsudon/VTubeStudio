VTube Studio has built-in post-processing, allowing you to add **"Visual Effects"** directly to the scene. This is available on **Windows** and **macOS**. Some effects work with [transparent streaming](https://github.com/DenchiSoft/VTubeStudio/wiki/Recording-Streaming-with-OBS), others don't.

You can combine effects, save effect presets and load those presets via hotkeys to switch between them.

:warning: **WARNING!** Some artists and riggers have voiced concerns about certain filters, mostly related to filters that distort the model in any way. Before using these filters, it is recommended to get permission from the people who made your model to prevent any potential disagreements with them in the future. :warning:

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_turn_on.gif" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_lens.gif" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_outline.gif" width="290" /> 
</p>

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_particle.gif" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_pixel_various.gif" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eff_eyes_b.gif" width="290" /> 
</p>

Effects include lens distortion, bloom, particles, overlays, various lighting effects and many more. You can configure and combine these effects however you want and then save your configurations as **VFX presets** that can be loaded at any time using hotkeys.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Some of the more fancy effects might be hard on your GPU and may not work smoothly on older PCs or laptops. If you want to combine many effects, you may need a decent GPU.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## Configuring effects

If you want to use **effects**, make sure you first turn them on globally using this switch. When you turn this **off**, all effects will be **disabled**.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/effects_main_window.png]]

Use the **"Select effects"** button to see a list of all available effects. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/effects_selection_list_1.png]]

From there, you can choose any effect in the list to turn it on/off and set its config values. The list will also show which effects are currently on.

## Effect Presets & Effect Hotkeys

After turning on and configuring a few effects, you can save that effect system state into an **"effect preset"** using the save button. That preset is then saved as a file in the `StreamingAssets\Effects` folder (the files have the extension `.effects.json`). Using the load button, you can load any previously created preset.

Presets are not bound to specific VTube Studio models, but you can set up **hotkeys** in your model to toggle effect presets or switch between them and their saved config values. All effects and effect config values are set up so switching between presets will **smoothly fade between the effects** when hotkeys are used.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/effects_hotkey_1.png]]

## Effects and transparent streaming

Some effects like lens distortion, snow/rain overlay and more work perfectly with transparency so using [transparent streaming](https://github.com/DenchiSoft/VTubeStudio/wiki/Recording-Streaming-with-OBS) with Spout2/Game-Capture/etc. works just fine.

Some other effects, like the shiny particle overlays, will not work properly though. If you want to properly use these effects, your stream background must be **in VTube Studio**. Remember that VTube Studio not only supports **.png** and **.jpg** backgrounds but also **.mp4** videos, so you can have your animated background directly in VTube Studio and even switch between backgrounds using **"Change Background" hotkeys**.

In addition to that, VTube Studio also supports **[Spout2 Backgrounds](https://github.com/DenchiSoft/VTubeStudio/wiki/Spout2-Background)**, which lets you set any Spout2 source as background in VTube Studio. That could for example be a Spout2 video stream sent directly from OBS.

## Effects and item pinning

Some effects distort your view of the model. Item pinning is based on your mouse cursor position, so when the model is distorted, it is not actually where it appears to be and manual pinning will not work as expected. Item scene hotkeys will still work though.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/effects_wave.png]]


## Effects and VNet

Active effects are currently **not** synchronized via [VNet](https://github.com/DenchiSoft/VTubeStudio/wiki/Multiplayer). That means if you activate effects on your side, people on the other side won't see them. They can have their own effects active.
