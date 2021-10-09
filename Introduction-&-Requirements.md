Thank you for giving **VTube Studio** a try!! <3

If you ever need help with the app, please reach out on Discord.

* [Discord](https://discord.gg/vtubestudio)
* [Twitter](https://twitter.com/VTubeStudio)
* [Mail](mailto:denchi@denchisoft.com)
* [Website](https://denchisoft.com)

## Basics

VTube Studio is an app available for **[iPhone/iPad](https://apps.apple.com/us/app/vtube-studio/id1511435444)**, **[Android](https://play.google.com/store/apps/details?id=com.denchi.vtubestudio)**, **[macOS](https://store.steampowered.com/app/1325860/VTube_Studio/)** and **[Windows](https://store.steampowered.com/app/1325860/VTube_Studio/)**. The app uses your smartphone or webcam to track your face and animate a [Live2D Cubism Model](https://www.live2d.com/en/) accordingly. 3D models are not supported. The model is shown directly on your phone or on your PC by streaming the face-tracking data over your local network from your phone to your PC/Mac.

**VTUBE STUDIO ONLY SUPPORTS LIVE2D MODELS. VROID/VRM IS NOT SUPPORTED. [PLEASE USE OTHER APPS LIKE VSEEFACE FOR THAT. YOU CAN USE VTUBE STUDIO TO CONTROL YOUR MODELS IN VSEEFACE USING HIGH QUALITY IOS TRACKING](https://github.com/DenchiSoft/VTubeStudio/wiki/Sending-data-to-VSeeFace/).**

<br/>

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_basic_setup_detail_small.png|alt="Basic VTS Setup"]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
Going purely by tracking quality, it's **iOS \> Webcam \> Android**

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## Where to download?

To run VTube Studio, you need to download the smartphone app (Android or iOS) and/or the desktop app on Steam (Windows or macOS). If you only want to use your webcam, you don't need the smartphone app.

[[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/download_steam.png|width=220px]]](https://store.steampowered.com/app/1325860/VTube_Studio/)
[[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/download_iphone.png|width=220px]]](https://apps.apple.com/us/app/vtube-studio/id1511435444)
[[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/download_android.png|width=220px]]](https://play.google.com/store/apps/details?id=com.denchi.vtubestudio)

* **Desktop (Steam)**
  * Windows/macOS: https://store.steampowered.com/app/1325860/VTube_Studio/
* **Smartphone**
  * iOS: https://apps.apple.com/us/app/vtube-studio/id1511435444
  * Android: https://play.google.com/store/apps/details?id=com.denchi.vtubestudio

## Is there a paid version? Why should I buy it?

Please check the ["How do I buy VTube Studio?"](https://github.com/DenchiSoft/VTubeStudio/wiki/FAQ) in the FAQ section.

## Supported Devices (iPhone/Android Tracking)

To run VTube Studio, you need a PC (Windows 7 and up) or Mac (10.14 Mojave and up) and a smartphone/tablet that supports the VTube Studio smartphone app. VTube Studio requires the augmented reality framework ARCore (from Google, on Android) or ARKit (from Apple, on iOS).

### Supported devices:
* **Android**
  * Any device that supports ARCore should work.
  * See https://developers.google.com/ar/discover/supported-devices
  * Some devices may not work despite ARCore being supported. When this happens, the camera preview will show a blue rectangle. You can try manually downgrading to older versions of ARCore and see if that helps, otherwise you'll have to wait until Google fixes support for your device in future versions.
* **iOS**
  * Any iPhone or iPad that has FaceID.
    * iPhone X, XR, XS (regular and Max)
    * iPhone 11, 12 or newer (regular, Pro and Pro Max),
    * iPad Pro (3<sup>rd</sup>, 4<sup>th</sup>+ generation)
  * Also supported: devices without FaceID but with the Apple A12 (or newer) Bionic Chip.
    * iPhone SE 2020
    * iPad (8<sup>th</sup> generation)

## Supported Devices (Webcam Tracking)

Any webcam will do, better picture quality means better tracking. Generally, a resolution of 1280x720 or above is recommended for good eye- and blink-tracking. Framerates between 15-30 FPS are sufficient for good tracking. Some users reported problems when using DSLR cameras.