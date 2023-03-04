The main use-case of VTube Studio is to use your smartphone for face tracking, render your model in the Mac/PC app and then use OBS (or recording similar software) to stream to YouTube or Twitch. Any Windows/Mac recording software should work with VTube Studio. 

If you use an iPhone/iPad for tracking, you can use WiFi or USB to stream the face tracking data to the PC app. On Android, you can only use WiFi.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
VTube Studio uses your local network (TCP/UDP) or USB to send face tracking data from your smartphone to your PC or Mac. Depending on your home network setup, there may be connection issues, most frequently caused by your firewall configuration. For more info, check out the chapter: 

[Connection Issues & Troubleshooting](https://github.com/DenchiSoft/VTubeStudio/wiki/Connection-Issues-%26amp%3B-Troubleshooting)
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]


## Streaming per WiFi - Preparation on PC/Mac

Streaming the face tracking data from your smartphone to PC/Mac is easy. First, make sure both your smartphone and PC/Mac are on the same local network, otherwise they will not be able to see each other.

Then, start the desktop app. In the settings, you can activate the server after choosing a port (please try leaving the default port first, 25565).

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/connection_server.png]]

This will start the VTube Studio server on your PC on every available network device. Since your PC may have multiple network devices, you may see multiple IPs when clicking the **"Show IP list"** button.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/ip_vx.png]]

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
While your IPv4 shown here is typically a local, internal address and cannot be publicly accessed over the internet, your IPv6 addresses are likely to be public addresses! Please be careful to block them out if you post screenshots on the internet. Stay safe!
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]
<br/>

When starting the server for the first time, you may see a popup from the Windows Defender Firewall. Make sure you click "Allow access" and "Private networks" is checked. Otherwise, your smartphone will not be able to connect to the PC app as connections will be blocked by the firewall.

The server is now active and is listening for connections from the smartphone app. Leave it this way.

## Streaming per WiFi - Connecting the Smartphone App

Next, start the app on your smartphone. In the settings, you can manually type in the IP and port from the desktop application or use the **"Find Server"** button to automatically scan for the server and use its IP and port. This scan should not take longer than 5 seconds.

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/server_scan.png" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/settings_main_2.jpg" width="290" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/smartphone_connected_real.png" width="290" /> 
</p>

Now, click "Connect to PC". The app will now connect to the server. If the connection is lost for some reason, the app will try to re-establish the connection automatically.

**Congratulations.** You are now streaming your face tracking data to your PC. You can now open a VTS model in the desktop application and it will use the face tracking data from the smartphone. You can also have the same or a different model open in the smartphone app at the same time if you’d like.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
You do not need to have a model open on your smartphone when streaming to PC. In fact, it is recommended to not have one open for performance reasons. When using "Streaming Mode", any opened models on your smartphone will be automatically unloaded when connecting.
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]

## Alternative to WiFi: Streaming per USB from iOS to PC/Mac

If you use an iPhone/iPad for tracking, you can also use a wired USB connection to send over the face tracking data in real time. This is very reliable and more stable than WiFi but also a newer feature so it’s now as well tested. Right now, this is the recommended way to stream face tracking data.

To start a connection, activate the "Connect USB" switch on your phone first. If a face tracking WiFi connection to your PC is active, this will also deactivate it as they cannot be running at the same time. Afterwards, activate the “Connect USB” switch in the app on your PC/Mac.  

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/usb_con_pc_1.png]]

If your device doesn’t show up or fails to connect, make sure all of the following are true.
* iOS device is connected to the PC per USB cable.
* iOS device is unlocked and running the VTube Studio app.
* The app on iOS says "USB started. Waiting for PC app to connect."
* The iPhone is "paired" with the PC (the phone must "trust" the PC). This can be checked by making sure iTunes can see the contents of the iPhone.
* **Important: Make sure you have installed iTunes!!** iTunes starts some background services on Windows/MacOS that are required for communication with iPhones. iTunes doesn’t have to be running, but make sure it is installed on your PC/Mac and has been started at least once. If the USB connection fails, try starting iTunes once before VTube Studio.

