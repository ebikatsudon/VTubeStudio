⚠️  **This is currently an unreleased/unannounced feature.** ⚠️ 

<br />

**Web Items** are a new item type available in VTube Studio.

A Web Item is essentially a full web browser, available as an item in VTube Studio. They can be moved, rotated and pinned like normal items but display a website that you can interact with. Under the hood, Web Items use the [Chromium Embedded Framework (CEF)](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework), so they have most of the functionality that Google Chrome has.

Web Items are basically like "OBS Browser Sources" (which also uses CEF), just directly in VTube Studio.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_a.png|alt="VTube Studio Web Items"|width=792px]]

Some basic info:

* Any website that works in Google Chrome will also work in VTube Studio Web Items.
* Like OBS Browser Sources, Web Items also support transparent page backgrounds. That way, you can use chat widgets, sponsor widgets, etc. directly in VTS easily.
* Like with a regular browser, you can log into websites, store data using cookies, etc. Logins/Cookies and other data can be remembered or cleared every time you restart VTS, depending on your Web Item settings.
* Sound is also supported (can be muted), so you could load Twitch/YouTube videos directly as pinnable items in VTS.
* Web Items also works with Item Scenes, so you can use hotkeys to load Web Items with certain presets/URLs.
* Web Items are **NOT** synced via [VNet Multiplayer](https://github.com/DenchiSoft/VTubeStudio/wiki/Multiplayer). They are only displayed on your side when you are in a collab.
* You can also use **hotkeys** to do stuff like spawn new Web Items, delete them or mute/unmute them.

## Quick access buttons

When you hover over the top right of the Web Item (see image above), a few buttons will be shown. Most should be self-explanatory. Some special buttons:

* `Settings button:` Opens the full settings page. This gives you access to all Web Item settings, such as item cropping, scroll sensitivity and more.
* `Lock button:` Lets you lock/unlock this Web Item. You should lock Web Items when interacting with their loaded web page, otherwise you'll also scroll/drag the item around.
* `Interaction button:` Turns web page interaction on/off for this Web Item. When you want to drag/move/scale a Web Item, you should turn interaction off because otherwise you'll also be interacting with the website at the same time.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_examples.png]]

## Hotkeys & Item Scenes

You can use hotkeys of the type `Trigger Web Item Action` to do various things with Web Items, such as:
* Spawn a new Web Item.
* Delete all Web Items.
* Mute/Unmute all Web Items.
* ...and more!

Also, Web Items also work with ["Item Scenes"](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-Scenes-and-Item-Hotkeys). That means you can set up Web Items and them save them into an Item Scene and then use hotkeys to load/unload these Web Items.

Web Items will be saved in Item Scenes including their URL, resolution, position, mute/unmute state, etc.

<p float="left">
  <img src="https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_item_scenes.gif" width="490" /> 
</p>

## Background transparency

Like OBS browser sources, VTube Studio Web Items support pages with transparent backgrounds. You can use this to put widgets like chat boxes or donation widgets and more directly into VTube Studio. The setting to enable/disable transparent backgrounds for a certain Web Item can be found in the full web item config.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_settings_a.png|width=613px]]

## Loading local files

Like Google Chrome, you can use Web Items to load local files (text, images, HTML pages, ...) or even browse local folders.

By default, this is turned off, so you have to manually allow your loaded Web Item to be able to load local files. Once you have done that, you can just use a local file path as URL for the Web Item and it will load.

Examples formats:
* `C:\Downloads\my_video.mp4` Will load the local video on the Web Item and play it.
* `C:\` Will show the contents of that folder. Be VERY careful with opening local folders. There could be personal information in there.
* `file://C:` Same as above, just using the `file://` prefix to open local files explicitly instead of implicitly.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_local.png]]

## Defaults

You can set defaults for some options like whether or not newly spawned Web Items should be muted or unmuted or whether or not new Web Items should be able to load local files.

These defaults can be set in the Web Item settings (scroll down a bit in the settings list).

## Limitations

Web Items have various limitations:

* They are *not synced via [VNet Multiplayer](https://github.com/DenchiSoft/VTubeStudio/wiki/Multiplayer)*. Syncing browser contexts would be extremely unsafe. Your Web Items will only show up on your side in collab sessions.
* Performance isn't optimal when playing high-resolution video in Web Items. It's recommended to keep the resolution of the Web Items at or below 1024 pixels if you experience performance issues or when playing multiple YouTube videos at the same time.
* Due to limitations imposed by CEF, zoom levels are shared per domain. That means that all Web Items that are on the same domain will have the same zoom level.

## Special file support (.mp4, .pdf, ...)

Web Items can directly display certain files, such as videos, music files or text files. This works regardless of where those files are stored (online or locally on your PC).

Supported formats include: `.mp4`, `.webm`, `.mp3`, `.bmp`, `.pdf`, `.txt`, `.html`, `.json`

You can also directly drag files of that type into the VTube Studio window. Doing so will load the file in a VTube Studio Web Item. Local file access will be automatically turned on for Web Items that were dragged into VTube Studio. Even when loading a picture file (for example a `.bmp`) that way, it is still a regular Web Item that will not be shared via VNet.

## Security

Web Items use the [Chromium Embedded Framework (CEF)](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework). That means opening a URL in VTube Studio Web Items is essentially as safe as opening the same URL in Google Chrome. 

That means Web Items are relatively safe, but you should never visit any suspicious sites or open random links sent by your chat.

Websites opened in Web Items are always blocked from accessing your webcam or microphone. For security reasons, there is no way to allow Web Items to access your webcam/microphone.

VTube Studio plugins cannot spawn Web Items via the API. Any website shown by Web Items has to be manually opened by the user (or opened via a previously saved Item Scene).

If plugins ever get access to Web Item functionality, it will be hidden behind an additional [permission](https://github.com/DenchiSoft/VTubeStudio/tree/master/Permissions).

## Web Items and the Steam Workshop

Web Items cannot be uploaded to the Steam Workshop.

## API access

One interesting aspect of Web Items is that they themselves could be VTube Studio plugins:
1. Load Web Item into the scene with URL `https://website.com/my_vts_plugin_url.html`
2. That website uses JavaScript to connect to the VTube Studio API.
3. The website is now an item in VTube Studio and connected to VTube Studio through the API at the same time.
4. The website can use the VTube Studio API to move, pin, unpin, delete, etc. its own item.
5. When the item is deleted, the browser process quits and the API connection is automatically disconnected.

*Note:* If the plugin wants to move, pin, etc. its own item, it needs to know the *item instance UUID*. Websites loaded in VTube Studio Web Items can receive that ID using JavaScript on page load like this: ["Item UUID Listener"](https://github.com/DenchiSoft/VTubeStudio/wiki/Web-Item-%E2%80%90-Item-UUID-Listener).

In general, API access related to Web Items is very limited:

* VTS plugins cannot spawn Web Items.
* You can use the API to move, pin and delete Web Items like normal items. 
* In the future, there may be more advanced functionality, such as letting plugins load URLs. If this is ever added, it will require an additional [permission](https://github.com/DenchiSoft/VTubeStudio/tree/master/Permissions) that has to be manually requested by the plugin and granted by the user.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_item_api_1.png|width=587px]]






