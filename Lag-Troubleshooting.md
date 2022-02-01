This page contains some things to try if VTube Studio lags on your PC.

**Please try all of this before asking in the VTube Studio Discord!!**

## Start VTube Studio as Administrator

On Windows, start VTube Studio as admin. VTube Studio can set its GPU priority to "high", which should prevent other GPU-hungry games from making it lag. However, this only works if VTube Studio is running as admin. You can start VTube Studio as admin like this: https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-as-Admin

## Check your logs

Click the orange "Log" button in the main menu in VTube Studio. Are there any errors? You can also see the full logs by checking the text files in the "Logs" folder next to your "Live2DModels" folder.

Sometimes something will break in VTS and spam the logs with errors every frame, causing the app to slow down a lot. If that is the case for you, please bring it up in the [VTube Studio Discord](https://discord.gg/VTubeStudio).

## Check the Windows Task Manager for performance issues (CPU/GPU usage)

Check the actual CPU/GPU usage in the task manager. If the total CPU or GPU usage is near 100% your PC, check which apps use most of it. If it's not VTube Studio but a game you're running at the same time, it's possible you'll have to adjust the settings of the game so your PC can handle running it and VTube Studio at the same time.

If the CPU/GPU usage is not near 100%, there might be some other issues unrelated to performance problems.

## Make sure Virtual Webcam and NDI are off in VTube Studio

If you're not using NDI or the Virtual Webcam, make sure they're both turned off in the VTS settings. Having them both on at the same time will cause performance issues and lag for sure.

If you're using one of them but the performance impact is too much, try using a normal OBS `Game Capture` instead.

## Try turning off other apps and check OBS

Is the lag only happening if you're recording in OBS (or if you have OBS on), or is it happening all the time, even if OBS isn't running? Is it happening if you use certain capture methods in OBS? Is it happening only with specific apps? This will be important information for further troubleshooting.

## Turn off NVIDIA G-Sync

NVIDIA G-Sync can cause issues, especially on multi-monitor setups. [Try turning it off like this](https://www.google.com/search?q=how+to+disable+nvidia+g-sync).

* Right-click on your desktop and click on `Nvidia Control Panel` from the menu.
* Click on the `+` next to Display.
* Select `Set up G-SYNC` (not all displays may have that)
* Uncheck the box next to `Enable G-SYNC`.

## Lower the game FPS

Make sure whatever game you're playing together with VTube Studio doesn't have the framerate set to unlimited. Try limiting the game FPS to 60 if possible. You can also try limiting the FPS directly in the `Nvidia Control Panel`, which should also work if the game doesn't have FPS settings.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/fps_setting_nvidia_control_panel.png]]

## Turn off "Hardware Accelerated GPU Scheduling"

HAGS can cause issues when running a game and VTube Studio at the same time. Check Google (or for example [this page](https://www.tenforums.com/tutorials/150440-turn-off-hardware-accelerated-gpu-scheduling-windows-10-a.html)) for info on how to do that.


## Check the framerate in VTube Studio

VTube Studio will show the actual render FPS when you open the logs in the app (orange "Log" button in the main menu).

If you have VSync on and use high-refresh-rate monitors, VTube Studio may be running at a very high FPS, causing performance issues when running games at the same time. Try limiting VTube Studio to `1/2 Refresh Rate` or `60 FPS` in the settings.

Generally, it's recommended to always run VTS at 60 FPS. This may cause screen-tearing in the app, but that will not show up in your OBS capture/stream/recording. 

## Turn off the Steam Overlay

Disable the Steam Overlay globally for all games. This has been shown to cause framerate issues for some users. You can turn it off like this (see `"Enabling the Steam Overlay"`): 

https://help.steampowered.com/en/faqs/view/3978-072C-18DF-FBF9

## Start VTube Studio without Steam

Try starting VTube Studio outside of Steam using the `start_without_steam.bat` file. For more info, see this Wiki page: ["Starting without Steam"](https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-without-Steam)

Also, try starting VTube Studio as admin and see if that helps. You can do that by right, clicking the VTube Studio `.exe` file, clicking `Properties` and checking `Run this program as an administrator` on the `Compatibility` tab. Then, you start it normally using Steam or using the `start_without_steam.bat` as described above.

## Set process priority and GPU priority for VTube Studio

Open the Windows Task Manager, go to the `Details` tab, right click `VTube Studio.exe` and select `High` or `Realtime` under the option `Set prioroty`.

If you don't see that tab, you might have to click `More details` at the bottom first.

## On laptops (and some PCs), set the "Preferred GPU" for VTS

Many laptops have a on-chip GPU (included in the CPU) and a dedicated GPU, which is typically much faster. It's possible that VTube Studio is running on the slower GPU. In Windows 10, you can set a "preferred GPU" per app.

[Check Google how to do that](https://www.google.com/search?q=set+preferred+gpu+windows+10) and set VTube Studio to run on your dedicated GPU. 

## Check the "Power Saving Mode"

Many laptops and some desktop PCs have "power saving modes". Having those on can greatly decrease performance. Make sure you don't have any mode like that active. If you're using a laptop, also make sure it's charging and not running on battery, as this sometimes also activates power-saving modes.

## Check your security/anti-malware software

If you're running antivirus- or other security-software, make sure VTS is added as an exception. One anti-malware app that is known to cause issues for VTS is "IObit Malware Fighter". Some anti-malware apps can cause VTS to run very slowly, so try deactivating them temporarily and see if that helps.

## Turn of all "performance improvement" apps (MSI AfterBurner, etc.)

Apps like `"MSI AfterBurner"` that improve game performance may actually cause performance/framerate issues in some cases. Turn them all off and see if that helps. If it does, check if you can add VTube Studio as an exception to those apps (they usually allow that somehow).

Another app that can cause lag is `"RTSS Rivatuner"`, so please be careful with that one as well.

## Make sure all software is up to date

Make sure all involved software is up to date. Especially the following:

* Your GPU (graphics card) driver
* OBS or whatever capture software you're using
* VTube Studio on Steam (make sure you're not on the beta branch)

## Reboot

Sometimes, this helps with fixing performance problems.

## If you have a multi-monitor setup

If you have a multi-monitor setup, try unplugging one monitor and see if that helps. If so, that could be valuable information for further troubleshooting in the VTube Studio Discord.

## Ask in the VTube Studio Discord

If none of that helped, please ask in the VTube Studio Discord by creating a support thread.

https://discord.gg/VTubeStudio












