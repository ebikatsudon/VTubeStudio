## Settings File

After clicking the settings icon (gear icon) in the main menu, the settings screen will be shown. It has several tabs, a help icon (links to this manual) and a language selector button that lets you change the interface language (app restart needed).

Global (not related to a specific model) setting are saved in this file:<br/>

`<VTS-App-Path>/VTube Studio_Data/StreamingAssets/Config/vts_config.json`<br/>

## General Settings (Misc.)

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_main_1.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_main_2.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_mouse.jpg" width="290" /> 
</p>

From here, you can purchase **VTube Studio PRO (iOS/Android only)**. On iOS, there is also a button to restore purchases on this screen.

Furthermore, there are some general settings for hiding the VTS logo, remembering the scene (save open background and model when restarting), etc.

Next, there’s the "Stream to PC" setup. This is for connecting your phone to your PC to stream the face tracking data to the PC app. This will be covered in the chapter **"Connecting your Smartphone to your PC/Mac"**. On iOS devices, you can also start an USB connection as alternative to WiFi here. This is recommended as it seems to be more reliable/stable than WiFi. On Android, this option is unfortunately not available.

Finally, there's the "Mouse Input Config". This allows you to use the mouse/finger position as input parameter to animate your model in addition to face tracking. You can select an **X-Range** and **Y-Range** in pixels. This range will be mapped to [-1, 1] for X and Y. With this setting, you could for example make your model follow your finger or mouse pointer with its eyes. This will also show mouse-clicks (right, left, middle) that can be used to trigger hotkeys. In the smartphone app, these mouse-clicks can be triggered by touching the screen with one finger (left-click), two fingers (right-click) and three fingers (middle-click). 

## General Settings (Voice-based Lipsync)

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/voice_lipsync.jpg]]

The voice-based lipsync options are only available on Windows and MacOS (except M1/Silicon Macs), you cannot use them on smartphones.

Voice-based lipsync enables you to do two things:

* **Open/Close mouth** (or any Live2D parameter) based on current microphone volume.
* **Change mouth shape** (or any Live2D parameter) based on detected frequencies in voice.

If microphone audio lags behind the values shown on the UI, use the "Reload" button to reload the selected microphone. Alternatively, you can use a hotkey to reload the microphone.

When enabled ("Use microphone" switch), you will be able to use three additional parameters in your VTube Studio model:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/new_params_voice.png]]

* **VoiceVolume:** Parameter between 0 and 1 depending on microphone sound volume.
  * **Volume Gain Slider** controls how strongly the volume affects this parameter.
  * **Volume Cutoff Slider** controls the minimum volume to still be picked up by the microphone. You can filter out background noise with this.
* **VoiceVolumePlusMouthOpen:** Combines **VoiceVolume** parameter with **value from tracking**. With this, you could for example make your mouth open when there's sound and when the face tracking sees the mouth as open. This parameter is also between 0 and 1.
* **VoiceFrequency:** This parameter is between 0 and 1 and sits at 0.5 per default. It goes up and down depending on the frequencies found in your voice. You can use this to control your mouth form.
  * **Frequency Gain Slider** controls how strongly the detected frequencies affect this parameter.

### How the VoiceFrequency Parameter is calculated:

When you speak, VTube Studio analyzes your speech and extracts the phonemes (**A, I, U, E, O, Other**) from your speech. You will see the squares at the bottom (see image above) turn dark when a specific phoneme is detected.

You can click each phoneme to turn it **red (-)**, **green (+)** or **neutral**. Depending on that, when this specific phoneme is detected, it will push the **VoiceFrequency **parameter up or down (and with that also your mouth shape, if you use this parameter).



