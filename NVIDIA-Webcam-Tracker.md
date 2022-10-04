### IMPORTANT: THIS FEATURE IS IN BETA. CURRENTLY IT CAN ONLY BE USED ON THE BETA BRANCH.

<br/>

In addition to tracking using OpenSeeFace, VTube Studio now supports high-quality, high-performance webcam tracking using the new **NVIDIA Broadcast Expression Tracker** for RTX GPUs.

<br/>

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/nvidia_broadcast_logo_full.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/rtx_on_smol.png]]

(art by [@GiruteaCafe](https://twitter.com/GiruteaCafe))

<br/>

This tracker is using GPU-accelerated NVIDIA machine learning technology, which makes it really fast and performant. Even at 60 FPS, the tracker uses very few CPU/GPU resources, so it's able to run smoothly along any other game.

<br/>

<img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/nvidia_tracker_example.gif" width="800" /> 

# How do I get the tracker?

This is currently only available on the beta branch. To get on the beta branch for VTube Studio, right-click VTube Studio in your Steam games list, click **"Properties"** go to the **"Betas"** branch and enter the password `broadcast1234`. This will unlock the beta branch "vts_nvidia_beta".

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/rtx_beta_explanation.png]]

# How to use this?

The NVIDIA Broadcast tracker can be started just like the regular OpenSeeFace webcam tracker. Just select **"RTX - NVIDIA Broadcast"** after clicking the **"Tracking Type"** button (see 1). This will only be available if you actually have a RTX-supported GPU.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/rtx_ui_explanation.png]]

1. Click this button to select the new NVIDIA Broadcast tracker. Will not be available if your GPU is not supported.
2. The tracking type. Only "Face Tracking" will be available here if you use the NVIDIA Broadcast tracker. Hand tracking is currently not supported when using the NVIDIA Broadcast tracker.
3. By activating **"Legacy Webcam Mode"**, you will use the old **DirectShow Windows API** to access the webcam instead of the new **Microsoft Media Foundation API**. This is not recommended, but depending on your webcam, webcam driver and Windows version, this can be more performant and use less CPU/GPU resources so feel free to give it a try!
4. Click this once after the tracking has initialized. Click while looking at the camera to set a neutral face pose and neutral blendshapes.
5. Click this to turn the external tracking preview window with the creepy face on or off (see 6).
6. The external tracking preview window. Can be useful for checking if the blendshapes are properly calibrated. Rendering the 3D face takes some CPU/GPU resources, so you should have it off most of the time if you don't need it. You can also close this window with the normal **"X button"** to turn it off.


# FAQ

## Will this be free?

It will be free (with the watermark) just like the regular webcam tracking. No additional purchase needed.

## Why am I not getting my full webcam FPS?

Up to 60 FPS, the tracker should be able to run at the full FPS supported by your webcam. If that is not the case for you, you can try the following:

### Make sure "Low-Light Compensation" is turned off

aaa

### Make sure "Anti-Flicker" is set to 60 Hz

aaa

### Make sure your camera actually supports that FPS

aaa

### Make sure you don't have the FPS limit slider set to something low in VTube Studio

aaa

### Try other video formats

aaa

### Run VTube Studio as admin

aaa

## How does this compare to iPhone/iPad tracking?

In terms of tracking quality, it's very similar. Mouth-tracking is very accurate and so is eye-tracking. Blink-tracking works well. Wink-tracking is fine too, but as always, depending on your eye shape/size it may work better or worse. You'll just have to try it out and see for yourself.

The face rotation range of the NVIDIA tracker is also very big so it's unlikely to lose tracking in most situations, even with fast face movement. I tried shaking my head really fast until I got a headache and never managed to make it lose tracking.

It supports the same parameters you have with iOS tracking, including **"Mouth X"** and **individual brow tracking**, but it **DOES NOT** currently support **cheek puff** and **tongue-tracking**. The tracker is in active development, so it is likely that those will be added eventually.

## So why would I still want an iPhone?

With the iPhone, all tracking is done entirely on the phone, so VTube Studio in your PC will run with minimal CPU/GPU usage. This new NVIDIA tracker is very performant, but there is still some CPU/GPU usage.

If you already have an iPhone and you're fine with the tracking and setup, I would recommend sticking with that.

Not having to use multiple devices is really nice though, so definitely give the new tracker a try as well, maybe it could be a good alternative for you.

## Is VBridger supported?

For the initial release, probably not. But I'll definitely give the VBridger-team access to everything required to make VBridger work with the new tracker so they can add support after the initial release if they want. We'll have to figure out how that's going to work, but there are a couple good ways I think. Shouldn't be too hard.

I do not have any plans to add blendshape customization or curve editors directly in VTube Studio.

## What CPU/GPU usage can I expect?

It depends on your CPU/GPU, but it should be fairly minimal, even at high framerates. On my RTX 3080, running the tracker at 60 FPS and at 1920x1080 webcam resolution, both CPU and GPU usage stay below 5%.

A lot of the tracking system (but not all of it) can be executed on the machine-learning-optimized **tensor-cores** of your NVIDIA RTX GPU. They aren't used by most video games, so they don't interfere with your gaming.

Will add more data here once more people test it with different GPUs.

## Will the NVIDIA Broadcast face tracker be improved?

The latest info I have from NVIDIA right now is that "virtual avatars and tracking" are a big priority for them right now, so it is likely that there will be improvements to this tracker (which is kind of a nice change seeing how Apple haven't ever updated their face tracking).

So improvements in quality/speed are likely.

## What about hand tracking?

That isn't currently supported with this tracker but NVIDIA are experimenting with various tracking types, so I would not be surprised if it's added eventually. I don't have any info about it though.

## What do I need?

The only requirement is a NVIDIA RTX Series GPU and a webcam (any webcam will do). All RTX GPUs are supported, so any RTX 20-series, 30-series or (upcoming) 40-series card will do, including laptop GPUs. GTX GPUs or GPUs from other vendors are not supported. Current Steam surveys show that about 30% of users have RTX cards and that number is increasing with each new NVIDIA GPU generation.

If you are not sure if you have an RTX GPU, please follow [this guide](https://www.tomsguide.com/how-to/what-graphics-card-do-i-have) to find out. If your GPU name starts with "NVIDIA GeForce RTX", you have a supported GPU.

## Does this work with glasses?

I've tried it with glasses and the eye-tracking and wink-tracking seems to work fairly well. Of course, it depends on the webcam placement and lighting too.

## Is the normal webcam tracking (OpenSeeFace) still available?

Of course! It is available and will always stay available. This is just another option you can try out.

## Can I use my existing models or do I need to change anything?

Parameter ranges/setups will be as close to iOS tracking as I can get them, so all your existing models should work without any changes (except cheek-puff and tongue-tracking since they are not available with this tracker for now).

## Should I buy an RTX GPU for this?

Up to you. The current OpenSeeFace tracker is already really good, so if that works for you, there's no need to update your GPU for now (unless you were going to do it anyway).

I would recommend waiting until the update is out and then check out the comparisons people will make. I think this new tracker is definitely a nice option to have available.

Also, if you already use VTS iPhone tracking or VBridger and you're happy with it, there is probably not much of a reason to change your setup for now.

## When can I test this?

This feature will be included in **VTube Studio 1.22.0**, which will be released in the **first week of October 2022**. There may be an open/closed beta before that, check the [Discord](https://discord.gg/VTubeStudio) for more info.





