VTube Studio supports hotkey activation on macOS even when the VTube Studio window is not in focus. However, this requires VTube Studio to read keyboard input in the background which isn't usually allowed for security reasons.

So, for this to work, you'll have to grant TWO permissions to VTube Studio. Both of those permissions will have to be active.

1. "Accessibility" permission.
2. "Input Monitoring" permission.

If those permissions aren't granted, background keypresses cannot be read. Make sure you activate them in the macOS system settings.

### 1. Add Accessibility permission

* Open macOS system settings.
* **Privacy & Security**  =>  **Accessibility**  => **Add VTube Studio to list and make sure toggle button is on.**
* Restart VTube Studio if it was running.

### 2. Add Input Monitoring permission

* Open macOS system settings.
* **Privacy & Security**  =>  **Input Monitoring**  => **Add VTube Studio to list and make sure toggle button is on.**
* Restart VTube Studio if it was running.

### How do I add VTube Studio to those permission lists?

You'll have to find the VTube Studio executable file in the Steam folder. Typically it is located here:

``Macintosh HD > Users > _username_ > Library > Application Support > Steam > steamapps > common > VTube Studio``

If you cannot find the `Library` folder in your user folder, make sure to unhide it like this: https://discussions.apple.com/thread/254002152?sortBy=best

⚠️ **Make sure VTube Studio is added to BOTH lists.** ⚠️ 

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/macos_acc_bg_3.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/macos_acc_bg_2.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/macos_acc_bg_4.png]]