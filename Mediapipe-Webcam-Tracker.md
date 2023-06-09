
<br/>

In addition to tracking using OpenSeeFace and the [NVIDIA RTX webcam tracker](https://github.com/DenchiSoft/VTubeStudio/wiki/NVIDIA-Webcam-Tracker), VTube Studio now supports high-quality webcam tracking using the new **Google Mediapipe Webcam tracker**. The quality is mostly comparable to the NVIDIA tracker but no special hardware is required.

It is directly included in VTube Studio (Windows only for now), no DLC or further download needed.

<br/>

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_A_small.png]]

<br/>

<img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_face_example_A.gif" width="800" /> 

# How do I get the tracker?

The tracker is only available for Windows, but unlike the NVIDIA tracker, no special GPU is required.

TODO: performance

# How to use this?

The NVIDIA Broadcast tracker can be started just like the regular OpenSeeFace webcam tracker. Just select **"RTX - NVIDIA Broadcast"** after clicking the **"Tracking Type"** button (see 1). This will only be available if you actually have a RTX-supported GPU.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/mediapipe_ui_explanation.png]]

1. Click this button to select the new NVIDIA Broadcast tracker. Will not be available if your GPU is not supported.
2. The tracking type. Only "Face Tracking" will be available here if you use the NVIDIA Broadcast tracker. Hand tracking is currently not supported when using the NVIDIA Broadcast tracker.
3. If you want to limit the tracking FPS, do it using this slider. Since VTube Studio interpolates the tracking data to 60 FPS, running the tracking above 30 FPS does not add much in terms of model movement quality.
4. Click this once after the tracking has initialized. Click while looking at the camera to set a neutral face pose and neutral blendshapes.
5. Click this to turn the external tracking preview window with the creepy face on or off (see 6).
6. The external tracking preview window. Can be useful for checking if the blendshapes are properly calibrated. Rendering the 3D face takes some CPU/GPU resources, so you should have it off most of the time if you don't need it. You can also close this window with the normal **"X button"** to turn it off.

Once the tracker has initialized and tracking has started, you can click the gray gear icon in the tracking preview screen (bottom right) to show the Windows webcam config window.

# FAQ

## Is this free?

It is free (with the watermark) just like the regular webcam tracking. No additional purchase needed.

## How does this compare to iPhone/iPad tracking?

In terms of tracking quality, it's very similar. Mouth-tracking is very accurate and so is eye-tracking. Blink-tracking works well. Wink-tracking is fine too, but as always, depending on your eye shape/size it may work better or worse. You'll just have to try it out and see for yourself.

The face rotation range of the NVIDIA tracker is also very big so it's unlikely to lose tracking in most situations, even with fast face movement. I tried shaking my head really fast until I got a headache and never managed to make it lose tracking.

It supports the same parameters you have with iOS tracking, including **"Mouth X"** and **individual brow tracking**, but it **DOES NOT** currently support **cheek puff** and **tongue-tracking**. The tracker is in active development, so it is likely that those will be added eventually.

## What CPU/GPU usage can I expect?

It depends on your CPU/GPU, but it should be fairly minimal, even at high framerates. On my RTX 3080, running the tracker at 60 FPS and at 1920x1080 webcam resolution, both CPU and GPU usage stay below 10%.

A lot of the tracking system (but not all of it) can be executed on the machine-learning-optimized **tensor-cores** of your NVIDIA RTX GPU. They aren't used by most video games, so they don't interfere with your gaming.

## What about hand tracking?

That isn't currently supported with this tracker but NVIDIA are experimenting with various tracking types, so I would not be surprised if it's added eventually. I don't have any info about it though.

## Does this work with glasses?

I've tried it with glasses and the eye-tracking and wink-tracking seems to work fairly well. Of course, it depends on the webcam placement and lighting too.

## Is the normal webcam tracking (OpenSeeFace) still available?

Of course! It is available and will always stay available as the main webcam tracker. This is just another option you can try out.

## Can I use my existing models or do I need to change anything?

Parameter ranges/setups will be as close to iOS tracking as I can get them, so all your existing models should work without any changes (except cheek-puff and tongue-tracking since they are not available with this tracker for now).


