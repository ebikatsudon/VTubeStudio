VTube Studio can use your microphone to analyze your speech and calculate Live2D model mouth forms based on it.

You can select two lipsync types:
* **Simple Lipsync**
  * Legacy option, Windows-only, based on Occulus VR Lipsync.
  * NOT RECOMMENDED, use **Advanced Lipsync** instead.
* **Advanced Lipsync:**
  * Based on [uLipSync](https://github.com/hecomi/uLipSync).
  * Fast and accurate, can be calibrated using your own voice so it can accurately detect A, I, U, E, O phonemes.
  * Available on all platforms (desktop and smartphone).

**Note:** "Simple Lipsync" will not be discussed here. If you're still using it, please consider moving on to "Advanced Lipsync". It supports the same parameters _and more_, is more performant and works on all platforms.

## Using Advanced Lipsync

To use **Advanced Lipsync** select it using the "Lipsync Type" button. Then select your microphone and make sure "Use microphone" is on.

There are three slider on the main config card:

* **Volume Gain:** Boost volume from microphone. Will have an effect on the `VoiceVolume` and `VoiceVolumePlusMouthOpen` parameters.
* **Volume Cutoff:** Noise gate. Eliminates low-volume noise. It's probably best to keep this low or at 0 and have a noise-gate before audio is fed into VTube Studio instead.
* **Frequency Gain:** Boost value for `VoiceFrequency` and `VoiceFrequencyPlusMouthSmile`. Those parameters are explained below.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_lipsync.png]]





