[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vtube_studio_plugins_logo.png|alt="VTube Studio Plugins Logo"|width=630px]]

**Note: To use plugins, you currently have to use the VTube Studio Beta. Plugins are not supported on smartphones. See [Discord](https://discord.gg/VTubeStudio) for more info.**

VTube Studio supports third-party **plugins** using the **VTube Studio API**. Some stuff plugins can do:
* Activate hotkeys (for example via Twitch donations, YouTube superchats, ...)
* Control face tracking parameters and control the model.
* Add entirely new tracking parameters and inject data for them, allowing for literally anything to control your model (software, game controllers, ...)
* Move the model, scale and rotate it.
* ...and more!!

A plugin could be an app running on your PC/Mac or even just a website that takes control of VTS running on your PC!!

_Plugins cannot access your webcam or read any personal data through VTS._

## Some examples of VTS plugins

For info on how to use those plugins, please check out the linked plugin websites. **Important: These plugins are UNOFFICIAL and are not developed by DenchiSoft. Please only use plugins you trust!!**
* a
* b
* c

Please reach out on [Discord](https://discord.gg/denchisoft) if you want your plugin added to this list.

## How to use plugins?

For info on how to use a **specific plugin**, please refer to the manual/website of that plugin or ask the plugin authors.

If you want to use plugins, first make sure the API (interface for the plugins) is turned on. It starts a local (websocket) server that plugins can then connect to. The server is started on port 8001 per default. If that port is taken (for example by another instance of VTube Studio), the server will be started on port 8002 and so on. You can also change the port manually. The number in parenthesis is the actual port the API was started on.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/plugins_on.png" width="600px"/>
</p>
<br/>

Now plugins (websites or apps running on your PC) can connect. Once connected, they will have to **request your permission first**. A popup will appear on screen once a plugin does that. If you deny it, the plugin can try requesting permission again at any time.

<br/>
<p align="center">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/plugin_permission.png" width="781px"/>
</p>
<br/>

You can view the list of all allowed plugins and confirm the plugin is on there now. Connected plugins will also be marked as "Active" on that list.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/plugin_list.png]]


## How to develop plugins?

## What are custom parameters?

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/custom_param_1.png]]