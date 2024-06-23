⚠️  **This is currently an unreleased/unannounced feature.** ⚠️ 

<br />

[**Web Items**](https://github.com/DenchiSoft/VTubeStudio/wiki/Web-Items) are just websites running in a browser, so they themselves could be VTS plugins and interact with VTube Studio directly. To interact with the VTS API (or at least with the item-related endpoints), the Web Item will need to know its own item instance UUID used to identify it inside of VTS.

For more general information about Web Items, check [this page](https://github.com/DenchiSoft/VTubeStudio/wiki/Web-Items).

To get that ID, you can use the following javascript. You have to send the message `vts_web_item_request_item_id` to VTube Studio like this:

```javascript
window.vuplex.postMessage('vts_web_item_request_item_id');
```

VTube Studio will then pass you the item UUID. You can use that ID to do stuff like move the item around, pin/unpin it, delete it (thus also closing the API connection since the browser process is shutting down) and more.

[[https://raw.githubusercontent.com/wiki/DenchiSoft/VTubeStudio/img/web_item_api_1.png|width=587px]]

```javascript
<!DOCTYPE html>
<html lang="en">
   <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>VTS Web Item ID Listener Example</title>
   </head>

   <body>

      <h1>VTS Web Item ID Listener Example</h1>
      <p id="messageDisplay">Waiting for message...</p>
      <p id="itemID">Waiting for item ID...</p>

      <script>
         if (window.vuplex)
         {
             addMessageListener();
         }
         else
         {
             window.addEventListener('vuplexready', addMessageListener);
         }
         
         function addMessageListener()
         {
             window.vuplex.addEventListener('message', function(event)
             {
                 let json = event.data;
                 let jsonParsed = JSON.parse(json);
         
                 // {"apiName": "VTubeStudioWebItemAPI", "messageType": "ItemID", "value": "129b5746777b4d5390ba8b36f4b4a515"}
                 document.getElementById('messageDisplay').textContent = 'Received JSON: ' + json;
                 document.getElementById('itemID').textContent = 'Item ID: ' + jsonParsed.value;
             });

             window.vuplex.postMessage('vts_web_item_request_item_id');
         }
      </script>
   </body>
</html>

```