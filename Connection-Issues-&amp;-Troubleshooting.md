Under normal circumstances, there should be no connection issues. There also should be no delay and no lag or hiccups/spikes. The streaming should be smooth and should have at most around 10 milliseconds of delay.

However, depending on your local network setup, there might be some issues. This chapter discusses possible causes and solutions.


## Possible Causes for Connection Issues

If you have trouble connecting your smartphone to the PC app (smartphone app is constantly stuck on "Connecting…" or server scan doesn't find anything), please work through the following list before asking questions on the [Discord](https://discord.gg/VTubeStudio). 

* Make sure there is no firewall blocking the connection. **In 90% of cases, this is what causes the connection problems**.
  * To test this, try temporarily turning off your built-in firewall (Windows Defender) and any additional network security software you have. If this fixes the issue, turn them back on and find out how you can add exceptions for VTube Studio (`"VTube Studio.exe"`). For Windows Defender, see the image below.
  * After downloading updates for the PC app, you may have to re-add it to the firewall exceptions.
* Make sure both devices (PC/Mac and smartphone) are on the same network.
  * This means both should be on the same WiFi. If the PC and/or smartphone are connected to your router via cable, that is fine too.
  * If your router has multiple WiFi networks available, make sure it is the same for your PC and smartphone. Also, try both networks.
* On Windows, make sure the used network is set to "Private" (see image below).
* Try turning off your Anti-Virus software temporarily.
* If "Updated" are shown as 0, you may have to restart the app once.
* If you have a VPN, see if there's an option related to "Invisible to Devices" switched on.
* Make sure iOS/Android and the app are up to date.
* Network extending devices and access points like Google Nest may cause problems.
* Check your router settings. Sometimes there are privacy settings activated that prevent devices from discovering each other.
* If your smartphone can't see your PC at all, there are issues with your network setup that you'll need to fix before VTube Studio can work. To test this, use a network discovery / "ping" app and let them run a discovery on your network.
  * Just search for "Network Scanner" on the respective smartphone app store. Any of those apps should work.
  * If you run into specific issues, try to Google them first before asking on Discord.
* Sometimes, VTube Studio reports the wrong server IP in the Steam version. Try opening a terminal on windows and type "ipconfig". If this shows IPs not listed in VTube Studio, try out all of them in the smartphone app.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/firewall_config.png]]



