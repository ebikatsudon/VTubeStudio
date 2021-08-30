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
* If "Updates" are shown as 0, you may have to restart the app once.
* If you have a VPN, see if there's an option related to "Invisible to Devices" switched on.
* Make sure iOS/Android and the app are up to date.
* Network extending devices and access points like Google Nest may cause problems.
* Check your router settings. Sometimes there are privacy settings activated that prevent devices from discovering each other.
* If your smartphone can't see your PC at all, there are issues with your network setup that you'll need to fix before VTube Studio can work. To test this, use a network discovery / "ping" app and let them run a discovery on your network.
  * Just search for "Network Scanner" on the respective smartphone app store. Any of those apps should work.
  * If you run into specific issues, try to Google them first before asking on Discord.
* Sometimes, VTube Studio reports the wrong server IP in the Steam version. Try opening a terminal on windows and type "ipconfig". If this shows IPs not listed in VTube Studio, try out all of them in the smartphone app.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/firewall_config.png]]

## Network Lag Troubleshooting (general)

If you experience lag or short breaks/freezes when streaming to PC, work through the following list:
* First, try restarting your router. That sometimes helps.
* Are you on WiFi?
  * In some extreme cases, your WiFi reception may cause lag or even very long (multiple seconds) delays in packets being sent over your network. Make sure you use 5GHz WiFi and not 2.4 as depending on your environment, 2.4 Ghz WiFi can have wildly unstable latency.
  * With WiFi, the latency still shouldn’t be higher than 10 milliseconds.
* If possible, use wired LAN connection instead of WiFi. This will give you a lag-free, 1-ms latency connection. You can use wired LAN on your smartphone using an adapter such as [this one for Android (USB-C)](https://www.amazon.com/dp/B0823CB5MT/) or [this one for iPhone/iPad](https://www.amazon.com/Lighting-Ethernet-Adapter-Network-100Mbps/dp/B07VK8Q36S/).
* Try changing the WiFi-channel that your router uses. When there are routers nearby sending on the same channel, this will cause lag/packet drop issues.
* If nothing helps, try out "ping" / "network analyzer" apps from your smartphone app store to analyze the network connection between your smartphone and PC. This often helps you understand when/why the freezes occur.


## Network Lag Troubleshooting (macOS and iPhone)

If you are on macOS and iOS, there might be some other causes: 
* Turn off location services, they will cause lag spikes periodically when your Mac scans your environment for WiFi networks. To turn that off, follow [this guide](https://osxdaily.com/2018/08/20/disable-location-services-mac/). 
  * https://osxdaily.com/2018/08/20/disable-location-services-mac/ 
* If you’re using WiFi, remove all unused WiFi-Networks from your list of known networks on both iPhone and Mac to stop them from scanning for them constantly. You can follow [this guide](https://9to5mac.com/2018/07/20/mac-how-to-forget-wireless-networks/).
  * https://9to5mac.com/2018/07/20/mac-how-to-forget-wireless-networks/
* When using iPhone and MacBook on WiFi: **Very important to turn off AirDrop on the Macbook**, because it **WILL** cause massive lag spikes when the iPhone is close to the Mac. Open a console and type: 
  * `sudo ifconfig awdl0 down`
* Later, when you’re done streaming, you can turn it back on by rebooting your Mac or typing this in a console: 
  * `sudo ifconfig awdl0 up`
* Turning off Bluetooth on your Mac and iPhone can also help. You can follow [this guide](https://support.apple.com/en-ca/guide/mac-help/blth1008/mac) to turn of Bluetooth on your Mac.
  * https://support.apple.com/guide/mac-help/turn-bluetooth-on-or-off-blth1008/mac 





