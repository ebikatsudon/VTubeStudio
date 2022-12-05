## What is the Tobii Tracker?

On **Windows**, you can use a [Tobii Eye Tracker 5 or 4C](https://gaming.tobii.com/product/eye-tracker-5/) to improve your eye- and head-tracking data.

Other Tobii trackers are **NOT OFFICIALLY SUPPORTED OR TESTED**.

These are special trackers you can attach to the bottom of your screen. They don't do any facial feature tracking (like mouth, brows, etc.) but they can provide **very accurate tracking** of your **head-position/rotation** and **eye-gaze-position** on your screen. 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/tobii_tracker_img.png|alt="Tobii Eye Tracker 5"]]

_**IMPORTANT:**_ If you use a **Tobii 4C Tracker**, you need to install the special beta driver version of **Tobii Experience** if you want to use head-tracking in addition to eye-tracking. For more info, check [this page](https://help.tobii.com/hc/en-us/articles/4408130344337-Head-tracking-is-no-longer-working-for-those-using-Tobii-Core). This will also be described in more detail below.

## How do I use it?

You can set up Tobii eye- and head-tracking on the following screen, only shown on Windows:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/tobii_basic.png|alt="Tobii Eye Tracker Setup"]]

Make sure your Tobii eye-tracker is connected to your PC and works (outside of VTube Studio). To make sure that is the case, follow the setup guide provided by Tobii for the tracker, including **installing all required drivers/software** and properly **calibrating the Tobii tracker**.

### For Tobii Eye Tracker 5

1. Go to https://gaming.tobii.com/getstarted/
2. Select `"Tobii Eyetracking"`
3. Select `"Tobii Eye Tracker 5"`
4. Click `"Download Driver"` and install it to install `"Tobii Experience"`.
5. Run `"Tobii Experience"` to make sure it works well with your device and calibrate it.

### For Tobii Eye Tracker 4C

For the Tobii 4C, **head-tracking is not supported unless you use the beta driver**. If you do that, you may lose some of the Tobii-Windows-Accessibility features.

If you don't use the beta driver, you will only have eye-tracking available in VTube Studio.

1. Go to https://gaming.tobii.com/getstarted/
2. Select `"Tobii Eyetracking"`
3. Select `"Tobii Eye Tracker 4C"`
4. Select `"Tobii Experience - beta only"`, then click `"Download Driver"` and install it to install `"Tobii Experience"`. If you don't want to install the beta driver, select `"Tobii Eye Tracking Core Software"` instead (but then you will not have head-tracking).
5. Run `"Tobii Experience"` to make sure it works well with your device and calibrate it.

## What can I do with it in VTube Studio?

VTube Studio can use the Tobii tracker to **improve** the head-tracking and eye-tracking coming from your webcam or iOS/Android device. Depending on the options you've turned on, it does the following:

* **Overwrite iPhone/webcam head X/Y/Z position and rotation** as long as the Tobii tracker detects the head.
  * This position/rotation is very smooth and accurate. Most importantly, it does **NOT** have that annoying head-nod when you blink.
* **Overwrite iPhone/webcam eye X/Y** as long as the Tobii tracker detects the eyes.
  * If this is turned on, VTube Studio will also make sure the eyes will never fully close as long as the Tobii-tracker still detects your eyes. This solves the problem of eyes closing when you look down, for example on your keyboard or drawing tablet. This works well because the Tobii tracker is below your screen and very accurate, so it will be able to tell if the eyes are still open.

You can also visualize the gaze position. This position will be shown as white bubble/circle in the VTube Studio window. The coordinates for the gaze circle are the X/Y gaze coordinates within the screen the tracker is installed on, so the shown position will only be accurate if VTube Studio is on that screen and in fullscreen mode.

## Can I use the Tobii tracker by itself without any other webcam/phone tracking?

That's possible, **but not recommended**. The Tobii tracker does not support things like brow/mouth/etc. tracking so if you use the Tobii tracker by itself, you're probably not going to get the general tracking quality you're looking for.

## I've got issues blinking/winking with my Tobii tracker

Make sure you haven't accidentally set the tracker to only track one eye. You can do that in the **Tobii Experience** app.


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/tobii_experience_eyes_on.png|alt="Tobii Eye Tracker Settings: Only track one eye"]]




