[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vtube_studio_plugins_logo.png|alt="VTube Studio Plugins Logo"|width=630px]]

**Note: Plugins are not supported on smartphones. See [Discord](https://discord.gg/VTubeStudio) for more info.**

VTube Studio supports third-party **plugins** using the **VTube Studio API**. Some stuff plugins can do:
* Activate hotkeys (for example via Twitch donations, YouTube superchats, ...)
* Control face tracking parameters and control the model.
* Add entirely new tracking parameters and inject data for them, allowing for literally anything to control your model (software, game controllers, ...)
* Move the model, scale and rotate it.
* ...and more!!

A plugin could be an app running on your PC/Mac or even just a website that takes control of VTS running on your PC!!

_Plugins cannot access your webcam or read any personal data through VTS._

## List of available VTube Studio Plugins

_Please reach out on [Discord](https://discord.gg/VTubeStudio) if you want your plugin added to this list._

For info on how to use those plugins, please check out the linked plugin websites. **Important: These plugins are UNOFFICIAL and are not developed by DenchiSoft. Please only use plugins you trust!!**
* **[Cheers Bot](https://cheers.hawk.bar/)**
  * By HawkBar
  * Trigger hotkeys, model changes and more based on Twitch stream events (donations, etc.)
* **[VTS React](https://vts-react.fugi.tech)**
  * By Fugi and Iron Vertex
  * Easy to use web-based Twitch/YouTube integration for VTube Studio.
* **[Mix It Up Streaming Bot](https://mixitupapp.com/)**
  * A versatile streaming bot that also supports VTS integration, including activating hotkeys on stream events such as donations, etc.
* **[VTChaos](https://github.com/Raelice/VTchaos)**
  * By Raelice
  * A YouTube/Twitch chat bot that sends commands to VTube Studio when someone uses certain commands in chat.
* **[VTube Studio Stream Deck Plugin](https://apps.elgato.com/search?s=vtube) (download via official Stream Deck app store)**
  * By Cazzar
  * Access all VTube Studio functionality directly using your Stream Deck, including triggering hotkeys and changing models.
* **[TP_VTS - Touch Portal Integration for VTube Studio](https://github.com/Wiccy84/TP_VTS)**
  * By Wiccy
  * Plugin that makes it easy to control VTube Studio using the Touch Portal smartphone app. Supports triggering hotkeys, loading and moving models, coloring ArtMeshes and more!
* **[VtubeStudioSimpleSETool](https://mononobe-monoko.booth.pm/items/3468381)**
  * By 物部モノ子
  * A VTube Studio plugin that can automatically play custom sound effects when tracking parameters reach certain values you can configure.
* **[Twitch Integrated Throwing System](https://remasuri3.itch.io/tits)**
  * By Remasuri32
  * A VTube Studio plugin that lets your viewers throw stuff at your model using Twitch redeems, etc. and have your model react accordingly like it's getting hit. 
* **[VTS-Puppet](https://eruben.itch.io/vtspuppet)**
  * By Eruben (@eruben_thillior)
  * This VTube Studio plugin lets you control your model using a gamepad, for example using an Xbox controller or Switch Pro Controller. You can move your model trigger hotkeys and more directly using your controller.
* **[VTSLivePlugins](https://github.com/fastestyukkuri/VTSLivePlugins)**
  * By 最速のゆっくり (@fastest_yukkuri)
  * This plugin lets you control your model using the current time of the day (seconds, minutes, hours, ...), movement of sun and moon and weather information from any place on earth. You could for example automatically change Live2D parameters based on the current time or weather.

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

You can view the list of all allowed plugins and confirm the plugin is on there now. Connected plugins will also be marked as "Active" on that list. The plugin now has full control over VTube Studio, so please only allow this for plugins from sources you trust.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/plugin_list.png]]

A given plugin has to only request permission once for a PC/Mac, so the permission-popup will not be shown the next time the plugin connects to VTube Studio, unless you have revoked the permission in the meantime. All plugin-related information is saved in the "Plugins" folder, which can be found in the "Config" folder next to the "Live2DModels" folder. Deleting the "Plugins" folder will also remove all permissions from all plugins.

## What are custom parameters?

Plugins can create **"Custom Parameters"**. Once created, the custom parameters will show up in VTube Studio exactly like normal face tracking parameters like `FaceAngleY` or `MouthX`, so you can use them to control Live2D parameters in your model. Plugins can freely create those parameters and inject data for them, so using any kind of hardware/software/controller/etc. to control parts of your Live2D model is easily possible.

Custom parameters are marked as such (blue color and P symbol) when selecting them as INPUT in the VTube Studio model config.

When a plugin is removed (revoked permissions by user), all custom parameters created by that plugin are also deleted, but they will still be set as INPUT if a model is using them. They will then be marked in red. The plugin can recreate those parameters at any time and the model will be able to use them again.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/custom_param_1.png]]

## How to develop plugins?

Anyone can develop plugins!! It's free and there are no restrictions! If you want, you can even sell your plugins. There are no royalties or licensing payments required to VTube Studio/DenchiSoft if you do.

If you're a developer and you're interested in making a plugin, please head over to the [VTube Studio API Development Page](https://github.com/DenchiSoft/VTubeStudio/) for all the details. If you have any questions, please ask in the API channel in the [VTube Studio Discord](https://discord.gg/VTubeStudio).

And most importantly, if you make something cool, please post videos on Twitter and tweet them at [@VTubeStudio](https://twitter.com/VTubeStudio)!! If it's something **really cool** and **user friendly** with a **good manual** I'd also like to feature it on this page.



