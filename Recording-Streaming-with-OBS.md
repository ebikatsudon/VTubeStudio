## Important!! Read this first.

* You should never use green-screen. VTube Studio supports *transparency* using various capture methods.
* On Windows, using Spout2 is recommended (see bottom of this page). It is fast and does not capture the VTube Studio UI.
* On macOS, use a normal game capture or NDI, which supports transparent video streaming as well. However, NDI may not be very performant.

## Recording with OBS (transparent background)

On your PC in VTube Studio, choose the **Color Picker background**. On Windows, you can use the "Transparent in capture" option here, which will make the window background transparent when the window is recorded in OBS **so you don’t need to use greenscreen/chroma keying**.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/obs_2.png|width=526px]]

**On macOS, this feature is not supported by OBS**, so choose any color you want here. You can remove that color from the video capture in OBS using a **"Chroma Key"** filter. Keep in mind that you can't use that color in your Live2D model, otherwise some parts of your model may be transparent as well.

Add a background in OBS, then add a capture for VTube Studio. To do that, select **"Game Capture"**. This supports transparent backgrounds but is only available on Windows.
On macOS, this option is called **"Syphon Client"**, but does not work after macOS 10.14 Mojave (see https://github.com/zakk4223/SyphonInject), so you need to use a regular window capture and a chroma key filter.

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/obs_4.png" width="394" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/obs_5.png" width="394" /> 
</p>

Your capture is now active. On macOS, you need to add a filter to remove the green (or whatever color you selected) background using **Right Click your capture → Filters → Add Filter → Chroma Key**.

You can now place your character anywhere on screen by moving/scaling/rotating it in directly in VTube Studio or in OBS.

Alternatively, you can use the **Virtual Webcam feature** or **NDI** in VTube Studio to create a webcam stream and then directly use that in apps like Zoom, Discord, etc. (see FAQ). 

## Using NDI for streaming to OBS with invisible UI (transparent background)

It is recommended to use OBS "Game Capture" to record the VTS window. Alternatively, you can use the Virtual Webcam or Newtek NDI (Network Device Interface) to create a video stream that can be used as input for software such as OBS.

The quality and latency of NDI streams is very good. It also supports a transparent background (no chroma/color key needed) and does not record the VTube Studio UI at all. CPU utilization of VTS may increase when using NDI. OBS plugins exist for macOS and Windows.

**OBS Plugin Page:** https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/

**OBS Plugin Download (Win/Mac):** https://github.com/Palakis/obs-ndi/releases/tag/4.9.1 

To use NDI, download the plugin from the GitHub-page linked above (.exe for Windows, .pkg for macOS) and install it. In VTube Studio, **activate the NDI toggle** in the **"Camera Settings" tab**. It is possible but not recommended to have NDI and the Virtual Webcam active at the same time.

VTube Studio lets you choose between NDI 4 and 5. It is recommended to use NDI 5 if it works without lag on your PC. By the way, NDI streams created by VTube Studio will be visible in your whole local network, so you could even have OBS running on a different PC and it will be able to read the NDI stream from VTube Studio (unless a firewall or network security settings prevent it).

Unlike with the Virtual Webcam, which only supports one stream, if you have multiple VTube Studio instances open, they will all show up as different (numbered) NDI sources in OBS.

In OBS, the following settings are recommended:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/obs_ndi.png]]

## Using the Virtual Webcam for streaming to OBS with invisible UI (transparent background)

This works similar to NDI. Just **activate the Virtual Webcam in the VTube Studio settings**, go to the color picker background and make sure you've checked **"Transparent in OBS"**.

In OBS, you should now see a webcam called **"VTubeStudioCam"**. Add it to your scene with the following settings (except the resolution):

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/obs_virtual_webcam_settings.png]]

## Using Spout2 for streaming to OBS with invisible UI (transparent background)


https://docs.offworld.live/#/obs-spout-plugin/README