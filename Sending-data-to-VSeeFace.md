You can use VTube Studio on your iPhone/iPad to send blendshape tracking data to [VSeeFace](https://www.vseeface.icu/) running on your PC, taking advantage of the high-quality iPhone tracking for your 3D models. This functionality is included in iOS version of VTube Studio **completely for free**, so you don't have to buy the PRO version if you want to use this feature (any support is of course appreciated regardless).

## What's VSeeFace?

VSeeFace is a free, highly configurable face and hand tracking VRM and [VSFAvatar](https://www.vseeface.icu/#vsfavatar) avatar puppeteering program for **3D Virtual YouTubers** (as opposed to Live2D) with a focus on robust tracking and high image quality, made by Emiliana ([@emiliana_vt](https://twitter.com/emiliana_vt)).

It mainly uses webcam tracking to control 3D VTuber avatars but has recently added support for high-quality iPhone tracking using various 3rd party apps, including VTube Studio.

You do not need VTube Studio on PC/Mac at all to use this feature. Your iPhone/iPad can directly connect to VSeeFace running on your PC over the local network (USB not supported).

If you are a 3D VTuber and have an iPhone, definitely give VSeeFace a try!!

## How do I use VTube Studio to control my 3D model in VSeeFace?

### Setting up VSeeFace

First, set up your 3D model like you normally would in VSeeFace. No special setup is required. All iOS blendshapes are supported when using VSeeFace with VTube Studio on your iPhone/iPad.

### Setting up VTube Studio

Next, [download](https://github.com/DenchiSoft/VTubeStudio/wiki/Introduction-&-Requirements) and start VTube Studio on your iPhone/iPad. For a list of supported iOS devices, check the page "[Introduction & Requirements](https://github.com/DenchiSoft/VTubeStudio/wiki/Introduction-&-Requirements)".

In VTube Studio, there are three icons in the main menu relevant for using the app with VSeeFace.

* **[1]:** Camera preview. Will show your face with the tracking mask.
  * **IMPORTANT: Click this at least once after installing VTube Studio on your iPhone/iPad, otherwise the tracking will not be initialized.**
  * You can leave this open or closed while using VTube Studio with VSeeFace.
* **[2]:** Quick-calibrate.
  * Instantly calibrates without showing the camera preview.
  * Will reset the current face position as "looking towards the camera".
  * VTube Studio can also be used in landscape mode, but make sure to run calibrating once after rotating your iPhone/iPad into landscape.
  * Calibration can also be triggered by having the camera preview open and clicking it.
* **[3]:** Settings/Config.
  * Only VSeeFace settings are relevant. They are on the first tab, all the way to the bottom.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vseeface_setup_1.png|alt="VSeeFace Setup Part 1"|width=1024px]]

To see the VSeeFace settings, open the settings from the main menu and scroll all the way to the bottom in the first config tab.

You will see the following settings:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vseeface_setup_2.png|alt="VSeeFace Setup Part 2"|width=512px]]

All you have to do here is turn on "Activate". VTube Studio is now ready to send blendshape data to VSeeFace. Once VSeeFace connects (and if you don't have the settings open), the screen will automatically dim to save energy. You can turn that off by deactivating "Streaming Mode" (scroll up a bit on the first settings tab, it's under "Stream to PC (WiFi)").

**Important:** To find out the IP/port you need for VSeeFace, press the "Show IP list" button.

### Connecting VSeeFace

Go back to VSeeFace running on your PC. Open the "Settings" and select "General Settings". Scroll down to this part:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vseeface_setup_3.png|alt="VSeeFace Setup Part 3"|width=1100px]]

Select "VTube Studio" in the tracking app dropdown menu and put in the IP/port you got from VTube Studio (that's your iPhone's IP). You should use the IPv4 here. The port is currently always **21412**.

Make sure the checkboxes for receiving all the data are checked, so "Receive facial features" (blendshapes), "Receive head movement" and "Receive eye gaze". If you're already using blendshapes for eye gaze, you may not want to check the last box.

VSeeFace should now automatically connect to VTube Studio and the tracking should be active. If you leave the tracking "active" when quitting the VTube Studio app on your iPhone/iPad, it will automatically start back up the next time you start VTube Studio.

Finally, scroll back up and check/optimize all other settings, such as various tracking sensitivities, gaze strength, etc.

In VTube Studio, it's recommended to keep the camera preview off and leave the screen all the way dimmed down to save energy and make sure the iPhone/iPad doesn't get hot. You can/should also charge it while using it. There should be no excessive heating under normal circumstances, especially not with newer devices. Older devices like the iPhone X can get kind of warm, but should not get hot.

## Troubleshooting (if iPhone/iPad can't connect)

If VSeeFace and VSeeFace can't establish a connection, that's usually related to some kind of network issue. It could be one of the following:

* Firewall or antivirus-app/security-software blocking the connection. Add an exception for VSeeFace or disable them temporarily to see if that fixes the issue. Make sure to re-enable them afterwards.
* Your PC and iPhone/iPad are not on the same WiFi/local network. If your router has multiple WiFi networks, try all of them.
* The network is not set to "Private" on your PC. Make sure it is.

All those issues and more are explained in detail on the page about [connection issues in VTube Studio](https://github.com/DenchiSoft/VTubeStudio/wiki/Connection-Issues-&-Troubleshooting). All of the issues listed on that page also apply to the VSeeFace connection.

You can find more info and VSeeFace-specific troubleshooting steps on the VSeeFace website, https://www.vseeface.icu/

## Where can I get help?

If you need help with VTube Studio, check the [VTube Studio Discord](https://discord.gg/VTubeStudio).

If you have any issues, questions or feedback for VSeeFace, please come to the **#vseeface** channel of [@Virtual_Deat](https://twitter.com/Virtual_Deat)’s discord server: https://discord.gg/BjBgk7k








