
## Can my face be accidentally revealed on stream?

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/accidental_reveal.png" />
</p>
<br/>

**No, that can't happen.** VTube Studio uses your smartphone camera just for face tracking and does not store or transmit your face or any raw face tracking data to your PC. Only the calculated parameters are transmitted, so at no point will any video be available on your PC. **The PC/Mac version also has no functionality whatsoever to reveal the webcam video.**

If you also want to make sure your face is never shown on your smartphone screen, make sure to set _"Camera Preview"_ to _"Never Show"_ (see [**"Camera Settings"**](https://github.com/DenchiSoft/VTubeStudio/wiki/VTube-Studio-Settings)).


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Don’t worry so much that people could see your face. You are beautiful! ♥
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## How do I buy VTube Studio? Why should I? Can I use it commercially?

There are two ways to purchase VTube Studio depending on how you want to use it.
 
* **I want to use iPhone/Android tracking only.**
  * First, download the VTube Studio app from the iPhone or Android App Store. The download itself is free. Then go into the app settings. There's a big button to buy the PRO version.
  * The PRO version gives you access to some features not available in the free version, such as being able to stream to your PC for longer than five minutes and being able to remove the VTube Studio logo in the app.
  * You do not need to purchase anything in the Steam version now, just download it for free and use it. No watermark is shown while using iPhone/Android tracking.

* **I want to use webcam tracking only.**
  * Download on Steam for free and try out the webcam tracking. You will notice a watermark being shown only when the webcam tracking is active.
  * Purchase the "remove watermark" DLC to remove the watermark.

If you want to use both webcam- and iOS/Android-tracking, you’ll have to buy VTS on iPhone/Android and Steam.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/watermark.jpg" width="552px"/>
</p>
<br/>


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
I know the watermark is super cute, but please buy VTube Studio regardless! Due to popular demand, you can now turn her back on by unchecking "Hide VTS Logo" in the settings. You can also add her to your scene as an item/asset using the item system.

By the way, the animation was made by Walfie (@walfieee) 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]


**As a private person/streamer, you are allowed to use VTube Studio commercially even without purchasing any PRO versions or DLCs.** This includes any kind of commercial use, including (but not limited to) monetized YouTube, Twitch, ..., streams, superchats, Live2D model commissions, etc. **If you can afford it and like VTube Studio, please support future development by purchasing it! <3**

This only applies to individual creators, smaller VTuber agencies and smaller companies in general. As a bigger company, you will need additional licensing. Please refer to the VTube Studio EULA for more information and/or contact us directly.

* **EULA:** https://denchisoft.com/license/
* **Contact:** denchi@denchisoft.com

## Can I try VTube Studio before buying it?

**You can and should!**

The app on Android and iOS itself is free and has a PRO version. The free version contains all features (including loading your own models), so please try VTube Studio first before purchasing.

On Steam, the app is free as well including all features. You only need to purchase the Steam DLC if you want to get rid of the watermark otherwise shown while using webcam tracking.

## Can I use my webcam for face tracking instead of my smartphone?

Yes, the Steam version supports webcam tracking.

## How can I use VTube Studio together with my friends?

You can start VTube Studio multiple times using the `start_without_steam.bat` file. Then you can use multiple webcams or multiple smartphones to control the models. You can also use one webcam to control multiple instances of VTube Studio.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/start_without_steam.png"/>
</p>
<br/>


If you want to do a collaboration stream with your friends over the internet, that is possible by using Zoom/Discord/Skype/etc. group video chat.

When using Discord for example, just have everyone use the Virtual Webcam feature of VTube Studio and then select that webcam as your main video chat camera in Discord. Alternatively, record using OBS and then use the OBS Virtual Webcam plugin to create a webcam stream for Discord. The person "hosting" the stream/collab can then record their Discord window using OBS, cut out everyone’s streams and use chroma key filters to remove the backgrounds. This works quite well, but you might need the high-quality 1080p video chat upgrade in Discord to get good picture quality.

**Note (experimental):** It is also possible to use VTS over the internet using LAN-Over-Internet tools like _Zero Tier One_ or _Hamachi_ (free up to 5 participants). You could start multiple instances of VTube Studio on the “host” PC and then have people connect to them. Just remember to use different ports for each instance! Disclaimer: I have not personally tested this method, but users have reported that it works. Of course, there may be network delay.

## Can I use USB instead of WiFi to connect my smartphone?

You can if you use an iPhone/iPad for face tracking. Direct face tracking data USB connection is not supported on Android. USB is very stable so this is the recommended way to send face tracking data.

On Android, as an alternative you could connect your smartphone via USB and the use USB tethering to put them in the same network even without WiFi.

**IMPORTANT:** This is unrelated to VTube Studio, but when you connect an iPhone to a PC/Mac via USB and you have a **Personal Hotspot** active, your PC will automatically try to use the iPhone mobile data connection to access the internet. See this for example: https://apple.stackexchange.com/questions/224069/iphone-prevent-automatic-hotspot-tethering-when-connecting-to-computer

## What is the "Virtual Webcam" feature?

**"Virtual Webcam"** (available on Windows only) allows you to record the VTube Studio window (without the UI) and directly make it available as a webcam stream, making it easy to use it in Discord, Zoom, etc.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/virt_webcam.png]]

First, you need to install the virtual camera by pressing the **"Install"** button. This should show a windows console popup and may ask you for administrator privileges, which you’ll have to grant. After successful installation, you can check the “Activate virtual webcam” option to start the webcam stream.

You can now select the stream as normal webcam in Discord, OBS, Zoom, etc. The name of the webcam is **"VTubeStudioCam"**. The virtual webcam also supports streaming with transparent background. Please note that the video quality with the virtual webcam might be slightly lower than what you would get when directly recording the window with OBS.

If the installation did not work, make sure to start VTube Studio as admin. If the webcam still does not show up (for example in OBS), **make sure OBS is also started as admin**.

## My device gets really hot! What is "Streaming Mode" in the smartphone app?

This is unfortunately normal. Your device may get really hot, but with the correct settings, it should not lead to any serious issues such as overheating or crashes. This mostly affects older supported devices, like the iPhone X.

To reduce heating, there are three things you should do when streaming to PC:
* **Unload your Live2D model on the smartphone.** You do not need to have a model loaded when streaming to PC and having a model open on your smartphone requires a lot of performance, which can be too much for some smartphones. 
* **Remove the camera preview.** Rendering the camera preview in the app can also cause some performance issues when done for a long time. Try turning it off.
* **Turn the screen brightness all the way down.** This will significantly reduce the heat produced by your phone.

When using these settings, **streaming for 15+ hours should be no problem** (keep the phone charged). Tested on iPhone X and iPad.

**"Streaming Mode"** automatically removes the model, removes the camera preview and lowers the screen brightness when connecting to your PC. It is recommended to always use streaming mode when streaming to your PC.

## Are there differences between the macOS and Windows version?

Windows supports all features. MacOS does not support transparent backgrounds with OBS and background hotkeys. This means hotkeys will only work on macOS if the VTube Studio window is focused. When for example playing a game at the same time, the hotkeys will not activate.

Also, webcam tracking for macOS is highly experimental and will most likely stay that way. Please keep that in mind when using VTube Studio for macOS.

## Why does my stream to PC/Mac lag?

This is almost always caused by network issues. As a first thing to try, restart your router/switches, PC and smartphone. If the issues persist, check the chapter ["Connection Issues & Troubleshooting"](https://github.com/DenchiSoft/VTubeStudio/wiki/Connection-Issues-%26amp%3B-Troubleshooting).

Sometimes, _"gaming performance improvement tools"_ like **Razer Game Boost** or **MSI Afterburner** can also cause performance issues, so try deactivating them and see if that improves things.

## Can I use my DSLR camera for webcam face tracking?

Should generally work but people have reported some issues. You may have to turn off **"USB selective suspend"** for some DSLRs. If the camera still doesn't work in VTube Studio, try tunneling it through OBS by using the OBS virtual webcam functionality and reading that virtual webcam with VTube Studio. This may cause performance issues on some PCs but it should work

## Why is the app running at crazy FPS (400+)?

This is a bug caused by some GPU drivers reporting incorrect display refresh rates, causing FPS to get unlocked when VSync is active in VTube Studio so it will try to render at the fastest possible speed.

To fix this, turn on G-SYNC in the Nvidia GPU settings (or the equivalent for your GPU). If that still doesn’t work, consider setting the FPS config to 60 in VTube Studio instead of VSync. 

## Why is blinking and eye tracking not supported on Android?

VTube Studio uses Google ARCore on Android. Eye/Blink/Wink-Tracking is not supported by this framework yet. There is no information if/when this will become available. It is possible that it will never be supported.

If and when it is added to ARCore, it will also be supported by VTube Studio

## I bought the PRO version on Android. Can I transfer it to iOS? Or Steam?

As a general rule, no. Technically, it is not possible as Google and Apple use different app-stores.<br/>
However, I may grant a grace period of one month.
 
If you purchased VTube Studio on Android and want to "transfer" that license to iOS, you can contact me per mail or on Discord. If you do, please first also purchase it on iOS and provide proof of purchase. I will then refund your purchase on Android. 
Transferring a purchase to/from Steam is also not allowed by Valve DLC guidelines. But if you use iOS/Android tracking, you do not need the Steam DLC because all it does is remove the watermark when using webcam tracking. No watermark is shown in the Steam version when using smartphone tracking.

## VTube Studio doesn't work on my smartphone. What can I do?

Please refer to the chapter [Introduction & Requirements](https://github.com/DenchiSoft/VTubeStudio/wiki/Introduction-&-Requirements).

## The face tracking is going crazy on my iPhone/iPad! What’s going on?

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/start_without_steam.png"/>
</p>
<br/>

First, try rebooting your phone.

If that doesn't help and the tracking mask in the camera preview is flying around or glitching out randomly, this is usually caused by magnetic interference. The iPhone/iPad uses a magnetometer (digital compass) to calculate the device facing direction. Please make sure your device does not have a case with magnets inside and is not leaning against a computer monitor. Having the device on a wireless charger may also cause similar issues.

In some instances, it can also be caused by bad lighting. Make sure you have good, non-colored lighting in your tracking setup. Some colors seem to confuse iOS/Android face tracking. Try going in a different room and see if that helps.

It has also been reported that mirrors somewhere in the camera view can confuse the tracking.

## Why does my iPhone/iPad show the forward-pointing camera?

This means your device is not supported. You should also have seen a popup telling you this when the app starts. For supported devices, see the chapter  [Introduction & Requirements](https://github.com/DenchiSoft/VTubeStudio/wiki/Introduction-&-Requirements).

## Are MacOS and Linux supported? What about M1 Macs?

* **Linux:** Not officially supported, but it's possible to run VTube Studio on Linux by using the `Network Tracker` mode and starting OpenSeeFace manually, see [this Trello item](https://trello.com/c/kbZWaoKN/26-variable-ip-for-osf-tracker). If you have questions about that, ask on Discord.
* **MacOS:** Supported experimentally with limitations. Download normally through Steam but please be aware that some functionality may not work, including stable webcam tracking and sound lipsync. Silicon M1 Macs should also work but there may be even more stability issues. I can only offer very limited support for macOS.

## Can I use VTube Studio in my company? How about for TV ads?

Depending on the size of your company, you may need additional licensing. Please see the [VTube Studio EULA](https://denchisoft.com/license/) or [contact me](mailto:denchi@denchisoft.com) for more information.






