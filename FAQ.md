
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

## My device gets really hot! What is “Streaming Mode” in the smartphone app?






