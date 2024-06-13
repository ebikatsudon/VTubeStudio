**Web Items** are a new item type available in VTube Studio.

A Web Item is essentially a full web browser, available as an item in VTube Studio. They can be moved, rotated and pinned like normal items but display a website that you can interact with. Under the hood, Web Items use the [Chromium Embedded Framework (CEF)](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework), so they have most of the functionality that Google Chrome has. Web Items are basically like "OBS Browser Sources" (which also uses CEF), just directly in VTube Studio.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_items_a.png|alt="VTube Studio Web Items"]]

Some basic info:

* Any website that works in Google Chrome will also work in VTube Studio Web Items.
* Like OBS Browser Sources, Web Items also support transparent page backgrounds. That way, you can use chat widgets, sponsor widgets, etc. directly in VTS easily.
* Like with a regular browser, you can log into websites, store data using cookies, etc. Logins/Cookies and other data can be remembered or cleared every time you restart VTS, depending on your Web Item settings.
* Sound is also supported (can be muted), so you could load Twitch/YouTube videos directly as pinnable items in VTS.
* Web Items also works with Item Scenes, so you can use hotkeys to load Web Items with certain presets/URLs.
* Web Items are **NOT** synced via VNet. They are only displayed on your side when you are in a collab.
* You can also use **hotkeys** to do stuff like spawn new Web Items, delete them or mute/unmute them.

## Quick access buttons

When you hover over the top right of the Web Item (see image above), a few buttons will be shown. Most should be self-explanatory. Some special buttons:

* `Setting button:` Opens the full settings page. This gives you access to all Web Item settings, such as item cropping, scroll sensitivity and more.
* `Lock button:` Lets you lock/unlock this Web Item. You should lock Web Items when interacting with their loaded web page, otherwise you'll also scroll/drag the item around.
* `Interaction button:` Turns web page interaction on/off for this Web Item. When you want to drag/move/scale a Web Item, you should turn interaction off because otherwise you'll also be interacting with the website at the same time.

TODO: Insert a few gifs here

## Hotkeys

## Item Scenes

## Background transparency

## Loading local files

## Security

## Limitations

vnet

resolution

## API access

may get access to set their own resolution, zoom, etc. if people want, will require special _permission_














