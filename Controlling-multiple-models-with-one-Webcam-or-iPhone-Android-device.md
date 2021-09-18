## Preparation

You can use one webcam or iPhone/Android device to control multiple VTube Studio instances.

To do that, you first have to start VTube Studio multiple times. You can do that using this button:

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/start_new_vts_instance_button.png"/>
</p>
<br/>

Alternatively, use the `start_without_steam.bat` file next to the main VTube Studio `.exe` file, see ["Starting VTube Studio without Steam"](https://github.com/DenchiSoft/VTubeStudio/wiki/Starting-without-Steam). Now you have VTube Studio running multiple times.

## Using one webcam to control multiple VTube Studio Instances

You can just select the same webcam multiple times in VTube Studio. The tracking will only be executed once, so there is no performance overhead when using the same webcam for multiple models.

## Using one iPhone or Android device to control multiple VTube Studio Instances

### When using iPhone/Android network tracking

Let's assume you've started 5 VTS instances. When starting the network server twice on the same port, VTube Studio will automatically choose the next available port and start it there instead. This will be indicated by a strike through the original port number.

The 5 instances run on the following ports:

* **(A)** "VTube Studio" - Port 25565
* **(B)** "VTube Studio Window 2" - Port 25566
* **(C)** "VTube Studio Window 3" - Port 25567
* **(D)** "VTube Studio Window 4" - Port 25568
* **(E)** "VTube Studio Window 5" - Port 25569

Note that all instances will have to have their network server turned on for this to work. You can now use your smartphone to connect to **any of those instances** by typing its port in the iOS app. Let's say you connect to instance **(B)** on port 25566. This instance then passes the tracking data on to the instance at `<own_port> - 1` and `<own_port> + 1`, so it passes the data UP and DOWN. The receiving instances then receive the data and pass it on, building a chain in both directions. If the chain is broken by having no VTube Studio instance running at one port, the data won't be passed on further than that.

This also means that if you want to use **two smartphones** to control **two different VTube Studio instances on the same PC**, the instances have to run at least 2 port numbers apart, otherwise the instances will try to send each other data.  

### When using an iPhone USB connection

This works a bit differently. **One instance receives the data via USB** and passes it on to **one other instance**. Let's assume we have the following 5 instances running:

* **(A)** "VTube Studio" - USB Server active, Network server turned off but port **25565 **selected.
* **(B)** "VTube Studio Window 2" - Port **25565**
* **(C)** "VTube Studio Window 3" - Port 25566
* **(D)** "VTube Studio Window 4" - Port 25567
* **(E)** "VTube Studio Window 5" - Port 25568

Note that both instances **(A)** and **(B)** have the same port selected for the network server. This works because instance **(A)** has USB active, meaning it can't have the network server active at the same time. Instance **(A)** receives the data via USB and passes it on to the port set in its (deactivated) network server. Instance **(B)** is running at that port and will receive the data and then pass it on DOWN and UP again, so to ports 25564 (nothing running there) and port 25566 (instance **(C)**). From there, the chain is continued normally.

