This page contains some things to try if your webcam doesn't work in VTube Studio. 

**Please try all of this before asking in the VTube Studio Discord!!**

## Check your logs

Click the orange "Log" button in the main menu in VTube Studio after turning on the webcam in the app. Are there any errors? You can also see the full logs by checking the text files in the "Logs" folder next to your "Live2DModels" folder.

## Try a different USB port

If it's a USB webcam, try plugging it into a different USB port. That sometimes helps.


## Try re-selecting the webcam in VTube Studio

Go to the webcam settings and select the webcam again. Then start the tracking.

## Make sure VTube Studio is allowed to access the webcam

Webcam access can be turned on/off for individual apps in the Windows settings. Some anti-malware apps also block apps from accessing webcams. Make sure VTube Studio is allowed to access the webcam and not blocked.

## Check any antivirus/security apps

Some antivirus- and other security-apps can block webcam access. Some do so by default. If you use any 3rd party antivirus-apps, check if they have webcam security settings. Some apps that have settings like that are `"ESET Antivirus"`, `"AVAST"` and `"IObit Malware Fighter"`.

For `"ESET Antivirus"` in particular, make sure to deactivate `Webcam Protection` like this:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/eset_antivirus_webcam_fix.png]]

## Install the Visual C++ Redistributable

This should happen automatically when you get VTube Studio on Steam, but sometimes it doesn't seem to work. Make sure you have it installed, otherwise the webcam tracking won't work and you'll get some error like `"Missing DLL"` in the logs.

You can get it here: (check the section "Visual Studio 2015, 2017, 2019, and 2022")

https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0

## Check if you're running a "Windows N Edition"

For example "Windows 10 N Edition". These versions lack some of the libraries required for the webcam tracking to work and you'll also get a `"Missing DLL"` error in the logs. You'll need to download some additional libraries.

Find the correct version for your Windows version from this page and install: https://support.microsoft.com/en-us/topic/media-feature-pack-for-windows-10-n-and-windows-10-kn-editions-229a1ad7-7a3f-87f7-9f0b-ff92fb96b3e4

## Make sure no other apps are using the webcam

Usually this will be shown in the VTS logs as `"No data from webcam - Maybe another app is using it?"`.

Often, VTS can't access the webcam because another app is still using it. This could happen if the camera is used in a scene in OBS, even if that scene is not open. Make sure your camera is used NOWHERE ELSE. For troubleshooting, I would also recommend just quitting all other apps/programs running on your PC and see if that helps.

## If you have a VPN, try turning it off

The webcam tracker used by VTube Studio (OpenSeeFace) uses the local network to communicate with VTube Studio. Because of that, VPNs might interfere with VTube Studio webcam tracking. Try turning off your VPN, then start VTS and see if that helps. If that fixes your problem, find a way to add VTube Studio to the list of exceptions of your VPN app.

## Reboot

Sometimes, this helps fix webcam problems.

## Do the Steam integrity check and check your security software

It can happen that security software deletes some files from the VTS directory that are required by the app to work. If you're running antivirus- or other security-software, make sure VTS is added as an exception. One anti-malware app that is known to cause issues for VTS is "IObit Malware Fighter".

To check if all files are there, run the Steam integrity check like this: https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB

Also make sure that VTube Studio is added as exception to your firewall and try turning off your firewall temporarily (remember to turn it back on again afterwards!!)

## Some devices cause issues, like the Avermedia Live Gamer Portable C875

For now, having this device connected to your PC will cause VTube Studio to crash when selecting webcams. You'll have to disconnect for a moment when selecting and starting the webcam in VTS, otherwise it won't work.

## Try moving the folder

Try moving the VTube Studio folder somewhere else. If it's somewhere in the `Program Files (x86)` folder, move it to the `Program Files` folder and see if that helps. You can always start VTube Studio without Steam like [this](https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-without-Steam).

## Check the `run.bat` file

Try starting the webcam tracker manually and see it it works outside of VTube Studio. You can do that by running the file `run.bat` in the folder `VTube Studio_Data\StreamingAssets\OpenSeeFaceTracker_v_1_20_2\binary` in your Steam files. This will show your webcam video including the tracking dots so don't do this on stream!! If this works but the tracker doesn't work in VTube Studio, that's an important clue for further troubleshooting.

## Ask in the VTube Studio Discord

If none of that helped, please ask in the VTube Studio Discord by creating a support thread. When creating a thread, please post your logs. The logs (.txt files) can be found in the `Logs` folder next to the `Live2DModels` folder.

https://discord.gg/VTubeStudio




