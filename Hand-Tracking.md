VTube Studio supports **experimental hand tracking using [Google MediaPipe](https://google.github.io/mediapipe/)**, currently **only on Windows**.

You can combine webcam hand tracking with webcam face tracking or smartphone face tracking.

The hand tracking parameters can be used to directly control Live2D parameters (including parameters for individual fingers) or to detect gestures that can then trigger hotkeys to activate gestures, animations and more.

Please keep in mind that this is an experimental feature and the tracking is far from perfect. There will likely be improvements in the future, but for the moment, it's definitely at least fun to play around with it.

## Activating Hand-Tracking

In the VTube Studio webcam settings, select either `Hand tracking only` or `Face and hand tracking`. If you use your iPhone for face tracking, you should select `Hand tracking only` here. Then turn on the webcam. Your hands should now be tracked. It my take a second for the tracker to pick up your hands.

Fast finger movements are okay, but fast hand movements make it lose tracking right away, so be careful with that.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_hands_1.png]]

The circles below the tracking preview show the finger angles (fully blue means finger is straight, fully white means it's fully bent). The bar below that shows the "hand-openness" for each hand. The two dots in the middle show the hand distance. All of these as well as the hand positions (relative to center) and hand angles can be used as tracking parameters ("inputs").

Below that, the detected hand gestures are being shown. The right and left hand can each have one gesture (shown left and right). Additionally, there are some special poses that require both hands. They will be shown in the middle.

## Using Gestures to trigger Hotkeys

On the hotkey tab, you'll find the button "Gesture". Clicking that button reveals the following window including a hand tracking preview:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_hands_2.png]]

Here, you can create a gesture-combination that will activate the hotkey. You can select one gesture for the left hand and one fore the right hand or a "dual-hand gesture" (triangle or "is-for-me" gesture). You can also just select a gesture for one hand.

You can choose if both hand gestures have to be detected for the hotkey to activate (using AND/OR) and configure whether or not the mirrored gesture is also allowed.

Finally, you can set a time that determines how long the gesture has to be detected for the hotkey to activate.

If the hotkey activates an expression, you can also set it so the expression is only active while the gesture is detected.

## Using the Hand Tracking Parameters as Inputs

You can use the hand tracking parameters as tracking inputs for your VTube Studio model to control Live2D parameters. Again, these can be unreliable so use with caution.

The following parameters are available:

* **Special**
  * `HandLeftFound`: 1 if left hand is currently tracked/found, 0 otherwise.
  * `HandRightFound`: 1 if right hand is currently tracked/found, 0 otherwise.
  * `BothHandsFound`: 1 if both hands are currently tracked/found, 0 otherwise.
  * `HandDistance`: The distance between the hands (if they are both found).
* **Hand Position**
  * `HandLeftPositionX`: X-distance to center (left hand).
  * `HandLeftPositionY`: Y-distance to center (left hand).
  * `HandLeftPositionZ`: Z-distance to center (left hand).
  * `HandRightPositionX`: X-distance to center (right hand).
  * `HandRightPositionY`: Y-distance to center (right hand).
  * `HandRightPositionZ`: Z-distance to center (right hand).
* **Hand Angles**
  * `HandLeftAngleX`: Left/Right rotation of left hand.
  * `HandLeftAngleZ`: Left/Right lean of left hand.
  * `HandRightAngleX`: Left/Right rotation of right hand.
  * `HandRightAngleZ`: Left/Right lean of right hand.
* **Fingers** (self-explanatory)
  * `HandLeftOpen`
  * `HandRightOpen`
  * `HandLeftFinger_1_Thumb`
  * `HandLeftFinger_2_Index`
  * `HandLeftFinger_3_Middle`
  * `HandLeftFinger_4_Ring`
  * `HandLeftFinger_5_Pinky`
  * `HandRightFinger_1_Thumb`
  * `HandRightFinger_2_Index`
  * `HandRightFinger_3_Middle`
  * `HandRightFinger_4_Ring`
  * `HandRightFinger_5_Pinky`

