

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

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_main_scene.png]]

## How do I reorder models?

You can drag/scale/resize your own model. You can drag using the left or right mouse button.
* **[LEFT]:** When you start a left-click drag, your model will be set to the top, above all other participant models. This will happen on your side and for all other participants. They can do the same to set themselves on top.
* **[RIGHT]:** You can right-click drag to drag your model without changing the model order.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_gif_drag.gif]]

## How do I see who has joined the collab?

Open the **"Session Control Screen"**. It's the right button.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_control.png|width=670px]]

This screen can safely opened during the session, since it shows no details like Steam ID, etc. It only shows the nicknames the participants have chosen. The host will be marked with a little crown there.

You can also leave the collab session from here. When the host leaves, the session ends and everyone disconnects.

**About the ping:** The ping is the time (in milliseconds) it takes for your movement data to be received by the host and for the host to respond to you. So by definition, the host will always have a 0 ms ping. 
Your ping will mostly depend on how far away you are from the host and also on whether or not you have a good internet connection. Typically it should be somewhere between 100 and 300 ms.

On this screen, you can do 4 things:
* **[1]:** Switch the model position control mode per participant (make other participants into Live2D items, explained below).
* **[2]:** Show/Hide models per participant. This is good for when only one person is streaming since your VTS won't have to render/animate the models from the other participants.
* **[3]:** Show/Hide items per participant.
* **[4]:** Set "smoothing" for that participant (might rename this to "movement buffer" since it's not really smoothing). This lets you set a buffer (between 0 and 1 seconds) for movement data. A bigger buffer allows VTS to remove stuttering caused by network lag but will also introduce a delay. Keep this at 0.05 (default) to 0.10 seconds if you don't experience any stuttering, otherwise increase it until the jittering is gone.

## How do I pin other participants to myself?

You can do that by switching on `"You control position"` for a participant. That essentially turns their model into a Live2D item that you can drag around, resize, rotate and even pin to yourself.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_gif_pin_to_other.gif]]

## I have frame-by-frame parameters in my Live2D model and they look broken for the other participants. How to fix that?

Try turning off `VNet parameter smoothing` for your frame-by-frame Live2D parameters. You can do that here:

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/vnet/vnet_param_smoothing.png]]

## Are there any limitations? For example for item/model sizes or Live2D items?

Currently, there are a few limitations in place, but you are unlikely to run into them if you use VNet normally.
* **[1]:** You can load any number of items, Live2D items or models.
* **[2]:** Any item/model you load can have at most 120 files.
* **[3]:** Any item/model you load can be at most 190 MB in total size (after VNet compression).
* **[4]:** Items/Models that have at least one file that is larger than 90 MB (compressed) will not work.
* **[5]:** You can load any number of Live2D items, but if the total number of Live2D parameters in your Live2D items is greater than 100, the Live2D item models that pushed the parameter count over 100 will not have their parameter values synced. They will still be loaded for the other participants though and react to physics on their side.
* **[6]:** Live2D parameter values can't be bigger than 9000 or smaller than -9000.
* **[7]:** All models/items are kept in memory, so if you load many very big items/models during the session, the VTube Studio RAM usage will grow, so be careful. There is currently no limit in place, so this can potentially crash VTube Studio.
* **[8]:** The collab time limit is 24 hours. After 24 hours, collabs automatically end and have to be restarted.

## Can I pin items to other people?

Currently you can't. I might consider adding that later.

## Can I modify my model settings during a collab?

It may work for some model settings. In general, I would not recommend it.

## Can I use this while playing a Steam game with friends?

Yes, you can run VTube Studio via Steam and any number of Steam games at the same time by normally starting them via Steam.

If the game uses the steam `"Invite to game"` feature, make sure you start the game **AFTER** VTube Studio. That marks the game as "currently played game" and all invites you send will be for that game.

## Something broke! What do I do?

Please remember that this feature is very new. There may be some bugs in the initial version.

Please report any bugs in the VTube Studio Discord: https://discord.gg/VTubeStudio  :heart:

## Why do I sometimes get disconnected from a collab?

That can happen for many reasons. A small hiccup in your internet connection can cause Steam to disconnect you from the collab. If you were the host, that means the collab instantly ends and everyone is disconnected. In that case, you'll have to restart the collab.

Other typical causes of Steam connection issues include:
* VPNs
* Anti-Virus / Anti-Spyware and other security apps (for example AVG)
* Firewalls
* App performance-improvement software
* P2P filesharing apps that consume a large amount of bandwidth
* Steam servers being temporarily unstable/down
* ...

For more info and troubleshooting, check out the official guide on Steam: https://help.steampowered.com/en/faqs/view/1F39-DCB4-FF28-5748

Also, Steam has a **weekly scheduled maintenance**, during which online services (including VTube Studio's VNet) will be unavailable for a short time. The maintenance happens **every Tuesday around 3-4 PM Pacific Time** and typically lasts for **10-30 minutes**. Please plan your collabs accordingly.

You can see current Steam status info on this website: https://steamstat.us/

## How safe is this? Can my models get stolen?

All security details can be found on the page "[[VNet-Security]]". In general, if you don't trust the other collab participants you should not use this, as they could use specialized software to steal your shared model during collabs (only models/items you load). This is true for VNet and any other collab application that shares your models with other participants. People outside the collab cannot steal your model.

VNet is just one more tool you can use in your collabs. In many cases, using video-sharing-based tools like [VDO.Ninja](https://vdo.ninja/), [Discord](https://discord.com/), [ping.gg](https://ping.gg/) or [MultiV](https://iv.gg/multiv/login) is the right choice.

If you're a security researcher and have found any vulnerabilities, please contact me at **support at denchisoft dot com** :heart:


