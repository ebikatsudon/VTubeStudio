⚠️ **This is currently in BETA and may not work as expected (or at all). Use at your own risk and keep backups of your models!!** ⚠️ 

⚠️ **This functionality is only useful for Live2D riggers!! If you are not a Live2D rigger, ignore this.** ⚠️ 

VTube Studio can connect directly to the Live2D Cubism Editor using the **Live2D Cubism External Application** functionality.

This makes the following integrations possible:
* You can send tracking data from VTS into the Live2D Cubism Editor. Having live real-time tracking movement in the Live2D physics preview window in Live2D Cubism makes setting up physics much easier since you can directly see how your physics setup reacts to face tracking movements without exporting the model.
* VTube Studio can automatically detect when you export models from the Live2D Cubism Editor. When a model is exported, VTube Studio can then automatically copy the model over into the VTube Studio model folder.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_api_editor_vts_2.png]]

## How to set this up

First, you have to make the Live2D Cubism Editor API is turned on. Select `File` => `External Application Integration settings...` and click the play icon to start the API.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_api_editor_1.png]]

Once that is done, start the connection to the Live2D Cubism Editor API in VTube Studio (first settings tab). If VTube Studio runs on a different PC than Live2D Cubism, you can also connect to the Live2D Cubism Editor API via the local network by turning on `"Editor runs on remote PC"` and putting in the local IP address of the PC with Live2D Cubism running on it. Make sure firewall exceptions are set up correctly for this to work.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_api_editor_vts_1.png]]

VTube Studio should now automatically try to connect/re-connect in the background. When it connects for the first time, you have to check the "Permission" checkbox in Live2D Cubism. Now, VTube Studio will have full access to the Live2D Cubism Editor API. VTube Studio will remember its own token so you only have to do this once.

Keep in mind that VTube Studio will send all Live2D parameter values of the currently loaded model to the Live2D Cubism Editor. So syncing model movements between VTube Studio and the Live2D Cubism Editor will only really work properly if models with the same Live2D parameters are loaded in both.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/live2d_api_editor_2.png]]

## Performance

VTube Studio will send all parameter values into the Live2D Cubism Editor every frame. For big models that run at low FPS in the Live2D Cubism Editor, this could freeze the editor entirely.

If that is the case for your model, it's recommended to only use the parameter sync functionality when the physics window is active in Live2D Cubism since the physics window usually runs smoothly.

To make sure VTube Studio only sends parameter data when the physics window is active, activate the `"Physics window only"` toggle.



