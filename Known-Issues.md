This is a list of known issues/bugs in the current version of VTube Studio

# Unsupported Device: Samsung S22 (any type)

Due to an incompatibility with the used tracking library, face tracking will not work on Samsung S22 devices. The library has since been discontinued, so there is nothing I can do to fix this.

I am always looking for replacements for that library, so as soon as I find something, I hope to restore compatibility.

# Unsupported Device: Samsung S23 (any type)

<s>When running the app on certain devices, the model textures show up all black, even the supposedly transparent parts.</s>

* <s>Confirmed devices: **Samsung SM-S916B (Galaxy S23+)**</s>
* <s>Confirmed OS: **Android 13**</s>
* <s>More details in VTS Discord thread: **https://discord.com/channels/652602255748497449/1076263423203086426**</s>
* <s>There is no indication in the logs showing anything going wrong.</s>
* <s>Bug tracking: **https://trello.com/c/T4A77kLC**</s>

<s>**Possible solution:** This may be happening due to the model using an unsupported texture type. Look into this further and provide sample builds with other texture types to the people experiencing this issue.
May be related to depth-buffer: https://stackoverflow.com/questions/72587842/rendertexture-in-unity-is-black-on-android-but-works-fine-in-editor
</s>

**Will be fixed with the next Android app update sometime around the end of May.**

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/bugs/broken_textures_s23.jpg]]

