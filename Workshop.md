VTube Studio lets you upload and download content using the **Steam Workshop**.

Currently, you can upload models and [items](https://github.com/DenchiSoft/VTubeStudio/wiki/Item-System) to the [Workshop](https://steamcommunity.com/app/1325860/workshop/).

## Workshop Rules

You can share any content on the VTube Studio Steam Workshop as long as you follow these rules:

* Do not share content that you are not allowed to share. Only share things you either made yourself or things that the creator explicitly allowed you to share.
* Do not share copyrighted content.
* Do not re-share any content you've downloaded from the Workshop.
* Do not use misleading content preview icons. Icons should not misrepresent the actual content.
* Do not share any sexual content or content containing explicit nudity. If it can't be shown on Twitch, do not upload it to the Workshop.

If your content breaks these rules, it may be banned from the Workshop.

## Sharing content

Before you can share/download content, you have to agree to the **Steam Workshop Agreement**: https://steamcommunity.com/sharedfiles/workshoplegalagreement

Once you've done that, make sure you have started VTube Studio through Steam and Steam is running and connected to the internet. Click the Steam icon in the main menu and select what you want to do.

If you want to share a model, **make sure that model is currently loaded**. If you want to share an item, **make sure that item is loaded** (only that item and no other item).

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_1.png]]

When sharing items, you can provide an artist. For models, you can provide a modeler and artist. They will both be shown when viewing the content in the Workshop search in VTube Studio.

If you want people to always credit you when they use your content, please indicate that by setting the switch accordingly. All of this data can be changed later by updating the Workshop content.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_2.png]]

Before the upload starts, you will see a list of files that will be uploaded. Please look through that list _carefully_ to make sure there's nothing in there that you don't want uploaded. VTube Studio will not upload any unrelated files that are not required for models/items to work (like .pdf and such).

If you have any model/art source files in there (like .cmo3 or .psd), VTube Studio will warn you before the upload and ask if you really want to share them.

After clicking "OK", the upload will start.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_3.png]]

After the upload, it may take up to 5 minutes (usually takes around 2) for the content to be searchable in the Workshop within VTS. You can also add additional preview images to the Workshop content by opening the Steam Workshop page in a browser and adding them there. These additional preview images will also be visible from within VTube Studio.

## Updating previously shared content

You can update all data of previously shared content, including metadata (artist, icon, etc.) and the actual files.

If you want to update the actual files, make sure you have the new files loaded when selecting the "Upload item/model" option. You will then have the option to add these new files on the upload screen.

## Downloading content

You can use various filters and sorting methods when searching for items/models on the Workshop.

Please be aware that anyone can upload content to the Workshop. Content that's not allowed (for example sexual content) will be removed, but that usually takes a while, so be careful when browsing the workshop and don't do it on stream.

There is also the option to search only for "verified" workshop content. This content is uploaded by people who make high-quality VTuber assets and can be considered stream-safe.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_4.png]]

The search results will then be shown in a list. You can upvote/downvote items directly from that list.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_5.png]]

After downloading models and items, they will be saved into the normal "Live2DModels" and "Items" folders. VTube Studio will also automatically subscribe to content on the Steam Workshop when you download them to keep track of what you've downloaded. However, VTube Studio will never auto-update any downloaded content. If the uploader updates an item/model, you have to re-download them manually to get the updates.

Downloaded content will follow a special naming pattern which identifies it as Workshop content and prevents items/models with the same name overwriting each other:

* **Models**
  * `<original-model-folder_name>`**\_workshop\_**`<workshop-id>`
  * Example: If the original model folder was `my_model`, it will become `my_model_workshop_1234567`, the number at the end being its Workshop ID
* **Items**
  * **workshop\_**`<workshop-id>`**_**`<original-item-filename>`
  * Example: If the original item file was `my_item.png`, it will become `workshop_7654321_my_item.png`, the number at the end being its Workshop ID

## Downloading random items from the Workshop into the scene

You can set up hotkeys for your model that download a randomly selected item from the Steam Workshop directly into the scene. It goes without saying that it's not recommended to do that live on Stream.

## Making sure you don't accidentally share models

Sharing models requires navigating through multiple menus and explicitly clicking "yes, I want to share this model" multiple times. It should be pretty much impossible to do it accidentally, but as an additional layer of security, there's a new switch that you can turn on that will prevent your model from being shared (will show "sharing this model is restricted" when you try).

If you are a Live2D rigger, I would recommend turning this on for models you send to your clients just to be on the safe side.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/workshop_vts_6.png]]




