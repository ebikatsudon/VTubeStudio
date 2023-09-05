VTube Studio can use your microphone to analyze your speech and calculate Live2D model mouth forms based on it.

You can select two lipsync types:
* **Simple Lipsync**
  * Legacy option, Windows-only, based on [Occulus VR Lipsync](https://developer.oculus.com/documentation/unity/audio-ovrlipsync-unity/)
  * NOT RECOMMENDED, use **Advanced Lipsync** instead.
* **Advanced Lipsync:**
  * Based on [uLipSync](https://github.com/hecomi/uLipSync)
  * Fast and accurate, can be calibrated using your own voice so it can accurately detect A, I, U, E, O phonemes.
  * Available on all platforms (desktop and smartphone).

**Note:** "Simple Lipsync" will not be discussed here. If you're still using it, please consider moving on to "Advanced Lipsync". It supports the same parameters _and more_, is more performant and works on all platforms.

## Using Advanced Lipsync

To use **Advanced Lipsync** select it using the "Lipsync Type" button. Then select your microphone and make sure "Use microphone" is on.

There are three slider on the main config card:

* **Volume Gain:** Boost volume from microphone. Will have an effect on the `VoiceVolume` and `VoiceVolumePlusMouthOpen` parameters.
* **Volume Cutoff:** Noise gate. Eliminates low-volume noise. It's probably best to keep this low or at 0 and have a noise-gate before audio is fed into VTube Studio instead.
* **Frequency Gain:** Boost value for `VoiceFrequency` and `VoiceFrequencyPlusMouthSmile`. Those parameters are explained below.

If your microphone lags behind, you can click the "Reload" button to restart the microphone. You can also set up a hotkey for that.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_lipsync.png]]

### Calibration

To calibrate the lipsync system, click each "Calibrate" button while saying the respecting vowel until the calibration is over. That way, the lipsync system will be calibrated to your voice. If you change your microphone or audio setup, you might want to redo the calibration.

Clicking "Reset" will reset the calibration to default values.

Make sure the calibration is good by saying all vowels again and checking if the respective vowel lights up on the UI.

The funny colorful visualizations shown next to the calibration buttons are related to the frequency spectrum recorded in your voice during calibration. If you'd like to learn more about the details, check the [uLipSync](https://github.com/hecomi/uLipSync) repository.

### Parameters and how to use them

The lipsync system outputs the following voice tracking parameters:

* `VoiceA`
  * Between 0 and 1
  * How much the `A` vowel is detected. 
* `VoiceI`
  * Between 0 and 1
  * How much the `I` vowel is detected. 
* `VoiceU`
  * Between 0 and 1
  * How much the `U` vowel is detected. 
* `VoiceE`
  * Between 0 and 1
  * How much the `E` vowel is detected. 
* `VoiceO`
  * Between 0 and 1
  * How much the `O` vowel is detected. 
* `VoiceSilence`
  * Between 0 and 1
  * 1 when "silence" is detected (based on your calibration) or when volume is very low (near 0).
* `VoiceVolume` / `VoiceVolumePlusMouthOpen`
  * Between 0 and 1
  * How loud the detected volume from microphone is.
  * Map this to your `ParamMouthOpen` Live2D parameter.
* `VoiceFrequency` / `VoiceFrequencyPlusMouthSmile`
  * Between 0 and 1
  * You would **NOT** use these parameters if you're already using the `VoiceA`, `VoiceI`, ... parameters. This is just an alternative for you if your model only has one mouth shape parameters so you can use this to combine the detected vowels into one single parameter.
  * Calculated based on the detected vowels. You can set up how the vowel detection values are multiplied to generate this parameter.
  * Map this to your `ParamMouthForm` Live2D parameter.


The `VoiceA/I/U/E/O` should be mapped to blendshape-Live2D-parameters called `ParamA`, `ParamI`, `ParamU`, `ParamE` and `ParamO` that deform the mouth to the respective shape.

Here's a rough reference for how you could set up your blendshape mouth forms to get the most out of the advanced lipsync setup. Depending on what your model/artstyle looks like, your mouth forms may look different.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vowel_ms.png]]







