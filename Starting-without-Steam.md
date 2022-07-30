VTube Studio is only available via Steam and all updates will distributed that way. However, once downloaded, **you can start VTube Studio without Steam**.

Use the `start_without_steam.bat` file next to the main VTube Studio `.exe`. 

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/start_without_steam.png"/>
</p>
<br/>

On macOS, it is located here: `~/Library/Application Support/Steam/steamapps/common/VTube Studio`. Since the "Library" folder is hidden on macOS, it can be a bit hard to access. Please take a look at this page for details on how to access it: https://forums.macrumors.com/threads/how-to-find-steam-apps-folder-location-on-mac.2303715/

### Starting VTube Studio multiple times

Using the `start_without_steam` file, you can even start VTube Studio multiple times.

If you have started VTube Studio once (with or without Steam), you can also start VTube Studio multiple times using the "Start VTube Studio" button on the first config tab.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/start_new_vts_instance_button.png"/>
</p>
<br/>

When you start multiple instances of VTube Studio, the ports for the network server and API you selected will already be taken, so they will be started on the next available port.

Then you can use multiple webcams or multiple smartphones to control the models. You can also use one webcam to control multiple instances of VTube Studio.
When you start VTube Studio multiple times, the windows will have different titles (Windows-only, not supported on macOS) so they can easily be captured separately by OBS.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vts_multi_window_title.png" width="730px"/>
</p>
<br/>

You can now use multiple webcams or smartphones (on different ports) to control the different VTube Studio instances. You can also use one webcam or iPhone/Android device in multiple VTube Studio instances so they use the same tracking data. In that case, the face tracking is only executed once so there is no additional CPU overhead.

To learn how to do that, please check out the page about [controlling multiple models with one webcam or smartphone](https://github.com/DenchiSoft/VTubeStudio/wiki/Controlling-multiple-models-with-one-Webcam-or-iPhone-Android-device).

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/multi_vts.gif" width="740px"/>
</p>
<br/>

If you've bought the `Remove Watermark DLC`, you'll have to start the app at least once with Steam, afterwards that DLC will also be available for use without Steam (and completely offline) on that PC.