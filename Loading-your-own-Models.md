VTube Studio comes with a few default models. Most of them belong to Live2D Inc., so please be sure to read the chapter **"Privacy Policy and Licensing"** if you want to use them in your streams.

This chapter covers how to load your own Live2D models into VTube Studio. It will be assumed that you already have your Live2D model finished and have a basic understanding what Live2D is and how it works (Live2D parameters, etc.)

## Preparing your Live2D model for VTube Studio

There isn’t really any specific special preparation you need to do with your Live2D model so it works with VTube Studio. As explained later in the chapter **"VTube Studio Settings"**, you can map any face tracking parameter to any Live2D parameter, so you could theoretically choose parameter IDs and ranges however you want.

However, it is recommended to adhere to the default IDs and parameter ranges (min/max). Please also note that only the Live2D parameter IDs matter to VTube Studio, not the Live2D parameter names.

When you’re done with your model, export it via **File → Export For Runtime → Export as .moc3 file**.

Make sure to choose the following settings:

* "Export Version" set to "SDK 3.0" or "SDK 3.3" or "SDK 4.0" (recommended).
* "Export Physics settings file (physics3.json)". If you don’t to this, your model will not have physics. Always export your physics file like this and never independently from the model, as this is the only way to make sure the physics file is "registered" with the model (in the .model3.json
file) so it’s usable by VTube Studio. If no physics file is registered, VTube Studio will use the first one it finds in the model folder.
* Export Types: SDK

This will create a folder with the following files (ignore the files marked red). If your model fails to load later in VTube Studio, make sure all files are there.


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/files_akari.png]]


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/open_data_folder.png]]


[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/auto_setup.png]]








