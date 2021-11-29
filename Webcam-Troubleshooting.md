This page contains some things to try if your webcam doesn't work in VTube Studio. 

## Check your logs

Click the orange "Log" button in the main menu in VTube Studio after turning on the webcam in the app. Are there any errors? You can also see the full logs by checking the text files in the "Logs" folder next to your "Live2DModels" folder.

## Make sure no other apps are using the webcam

Usually this will be shown in the VTS logs as `"No data from webcam - Maybe another app is using it?"`.

Often, VTS can't access the webcam because another app is still using it. This could happen if the camera is used in a scene in OBS, even if that scene is not open. Make sure your camera is used NOWHERE ELSE. For troubleshooting, I would also recommend just quitting all other apps/programs running on your PC and see if that helps.

## Reboot

Sometimes, this helps fix webcam problems.

## Do the Steam integrity check and check your security software

It can happen that security software deletes some files from the VTS directory that are required by the app to work. If you're running antivirus- or other security-software, make sure VTS is added as an exception. One anti-malware app that is known to cause issues for VTS is "IObit Malware Fighter".

To check if all files are there, run the Steam integrity check like this: https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB

## Some devices cause issues, like the Avermedia Live Gamer Portable C875

For now, having this device connected to your PC will cause VTube Studio to crash when selecting webcams. You'll have to disconnect for a moment when selecting and starting the webcam in VTS, otherwise it won't work.

## Install 
- install c++ runtime
- check windows N
- make sure webcam is allowed in windows
- check run.bat