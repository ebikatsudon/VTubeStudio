## What is the Tobii Tracker?

On **Windows**, you can use a [Tobii Eye Tracker 5 or 4C](https://gaming.tobii.com/product/eye-tracker-5/) to improve your eye- and head-tracking data.

These are special trackers you can attach to the bottom of your screen. They don't do any facial feature tracking (like mouth, brows, etc.) but they can provide **very accurate tracking** of your **head-position/rotation** and **eye-gaze-position** on your screen. 

You can set if up on the following screen, only shown on Windows:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/tobii_basic.png|alt="Tobii Eye Tracker Setup"]]

## How do I use it?

Make sure your Tobii eye-tracker is connected to your PC and works (outside of VTube Studio). To make sure that is the case, follow the setup guide provided by Tobii for the tracker, including **installing all required drivers/software** and properly **calibrating the Tobii tracker**.

## What can I do with it in VTube Studio?

VTube Studio can use the Tobii tracker to improve the head-tracking and eye-tracking. Depending on the options you've turned on, it does the following:

* Overwrite iPhone/webcam head X/Y/Z position and rotation as long as the Tobii tracker detects the head.
  * This position/rotation is very smooth and accurate. Most importantly, it does NOT have that annoying head-nod when you blink.
* Overwrite iPhone/webcam eye X/Y as long as the Tobii tracker detects the eyes.
  * If this is turned on, VTube Studio will also make sure the eyes will never fully close as long as the Tobii-tracker still detects the eyes. This solves the problem of eyes closing when you look down, for example on your keyboard: because the Tobii tracker is below your screen and very accurate, it will be able to tell if the eyes are still open.







