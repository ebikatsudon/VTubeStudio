
<br/>

In addition to tracking using OpenSeeFace and the [NVIDIA RTX webcam tracker](https://github.com/DenchiSoft/VTubeStudio/wiki/NVIDIA-Webcam-Tracker), VTube Studio now supports high-quality webcam tracking using the new **Google Mediapipe Webcam tracker**. The quality is roughly comparable to the NVIDIA tracker but no special hardware is required.

It is directly included in VTube Studio (Windows only for now), no DLC or further download needed.

<br/>

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_A_small.png]]

<br/>

<img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_face_example_A.gif" width="800" /> 

# How do I get the tracker?

The Google Mediapipe tracker is only available for Windows, but unlike the NVIDIA tracker, no special GPU is required. The tracker is directly included in VTube Studio, no further download or DLC needed.

# How to use this?

The Google Mediapipe tracker can be started just like the regular OpenSeeFace webcam tracker. Just select **"[Google] Mediapipe Tracker"** after clicking the **"Tracking Type"** button. This will only be available on Windows.

After starting the tracker for the first time, make sure to calibrate at least once while making a neutral face and looking straight at the screen. VTube Studio remembers the calibration data so you don't have to do that every time you start the tracker or restart VTube Studio.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_ui_explanation.png]]

# FAQ

## How does this compare to NVIDIA/iPhone/iPad tracking?

In terms of tracking quality, I would say it is pretty good but not quite as good as the NVIDIA tracking. With further updates, it could definitely get as good, if not better. I will also look into bringing this to the Android version of VTube Studio.

Mouth-tracking is pretty accurate and so is eye-tracking. Blink-tracking works well. Wink-tracking is fine too, but as always, depending on your eye shape/size it may work better or worse. You'll just have to try it out and see for yourself.

The face rotation range of the Google Mediapipe tracker is a bit more restrictive than most other trackers. If you look too much down or left/right, it may lose tracking.

It supports the same parameters you have with iOS tracking, including **"Mouth X"** and **individual brow tracking**, but it **DOES NOT** currently support **cheek puff** and **tongue-tracking**. The tracker is in active development, so it is likely that those will be added eventually.

## What CPU/GPU usage can I expect?

It should be comparable to the OpenSeeFace webcam tracking in terms of CPU/GPU usage.

## What about hand tracking?

Hand tracking is supported when using the Google Mediapipe tracker.

## Does this work with glasses?

I've tried it with glasses and the eye-tracking and wink-tracking seems to work fairly well. Of course, it depends on the webcam placement and lighting too.

## Is the normal webcam tracking (OpenSeeFace) still available?

Of course! It is available and will always stay available as the main webcam tracker. This is just another option you can try out.

## Can I use my existing models or do I need to change anything?

Parameter ranges/setups will be as close to iOS tracking as I can get them, so all your existing models should work without any changes (except cheek-puff and tongue-tracking since they are not available with this tracker for now).


