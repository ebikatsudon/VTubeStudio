

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/akaridance_anim.gif" width="110" /> 
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_icon_text_dark.png" width="200" /> 
</p>

**VNet** is VTube Studio's built-in **online collaboration functionality**, available as **paid DLC** for Windows and macOS.

You can buy it here: https://store.steampowered.com/app/2384550

* It works for **up to 4 people** per collab session.
* You HAVE to **start VTube Studio through Steam** to use VNet.
* Any models and items (including Live2D Items) you load are **automatically synced to other participants**. There are currently no restrictions as to how many you can load.
* With this, your collab participants will **show up directly in your VTS**, so you no longer have to deal with bad collab video quality.
* You can even **pin other participants' models to yourself**.
* Movement data is sent between participants via the Steam P2P network, so you have to be logged into Steam to use this and the person hosting the collab has to be **Steam-friends** with all participants.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
**Note:** This page describes what VNet is and how to use it. If you want to learn about security aspects, please check out the page "[[VNet-Security]]".
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]


## How do I host/join a session?

There are two new buttons in the main menu:
* **[LEFT]: Collab Setup**
  * Use this for setting up or joining the collab. Will show private details such as Steam names, Steam IDs and Steam profile pictures.
* **[RIGHT]: Collab Control**
  * Use this during the collab. Will show who's in the collab but only shows nicknames and no personal info.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_main_buttons.png]]

In the `collab setup screen`, you can choose if you want to host or join a session. Then, choose a nickname. This will be used to identify you during the session and will be shown instead of your Steam name or Steam ID since many people may want to keep those private.

Make sure you put in the correct password and all people on the collab use the same version of VTube Studio. Then, to host/join:
* If you are HOSTING a collab, you can select up to 3 Steam friends to add to the collab. ---> Then press `Host` button.
* If you are JOINING a collab, you have to select the Steam friend who is hosting the collab you want to join.  ---> Then press `Join` button.

You can also select a `File Server Region`. This determines which VNet server your files will be uploaded to. Choose the nearest region to you so your models/items upload as fast as possible.
The host can also set the `Data FPS`. This determines how fast movement data is sent between collab participants.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_top.png]]
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/bunny_point.png|alt="Important Point!!"|height=59px|width=189px]]<br/>
The person with the best internet connection (upload/download speed) should host the session!
[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/hint_bottom.png]]


In the top right, you can access the general collab settings. This lets you disallow sharing dragged-in items, for example (as a security measure).

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_basic_setup.png]]

You will then be shown a list of all other clients in the collab and can decide whether or not you want to join.

If you decide to join, you are now in the collab session. Any models/items you load will automatically synced to all other participants.

This screen will show the ping for all joined clients and whether or not they're currently uploading/downloading any items/models in the background. A red dot next to their profile picture means they haven't currently joined the collab.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_users_list.png|height=430px]]

When people join, their models/items will spawn in automatically and vanish when they leave.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_main_scene.png|height=400px]]

## How do I reorder models?

You can drag/scale/resize your own model. You can drag using the left or right mouse button.
* **[LEFT]:** When you start a left-click drag, your model will be set to the top, above all other participant models. This will happen on your side and for all other participants. They can do the same to set themselves on top.
* **[RIGHT]:** You can right-click drag to drag your model without changing the model order.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_gif_drag.gif]]


## Why do I sometimes get disconnected from a collab?

https://help.steampowered.com/en/faqs/view/1F39-DCB4-FF28-5748