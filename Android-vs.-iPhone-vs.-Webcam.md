The smartphone face tracking is provided by Alter Mocap4Face on Android and Apple ARKit on iOS. ARKit face tracking on iOS is very accurate and fast. The Android-tracking is also pretty good but lacks behind the accuracy of the iOS tracking at the moment. This is partially due to the supported iOS devices having specialized hardware for face tracking (TrueDepth Camera). iOS devices with the A12 chip or newer without the TrueDepth camera are also supported and the tracking quality is roughly the same. Some minor differences may be observed when using the devices in environments with very bad lighting.
 
In short, iOS devices are generally better. They provide much smoother and more detailed tracking. Newer iPads or iPhones are generally preferable over older ones, as old ones may get warm/hot during usage (see also FAQ). Furthermore, some important features are not supported on Android. If you can, I’d recommend getting a recent (newest gen) iPhone/iPad. 
 
Webcam tracking is really good as well but has some disadvantages. Mainly, it puts additional strain on your CPU that you wouldn’t have when the tracking is performed by a connected phone. Also, blink- and eye-tracking are not as accurate as they are on iOS. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/device_difference_table.png|alt="Tracking device differences"]]

To add to that, the tracking on iOS is less shaky and needs less smoothing. This results in your model reacting a bit faster and movement looking more natural in general.

**To summarize, if you want to take advantage of high-quality face tracking, the iOS version is the way to go but webcam tracking is also very good and may make things easier for you if your PC is powerful enough to run it.**