⚠️  **This is currently an unreleased/unannounced feature.** ⚠️ 

**Web Items** are just websites running in a browser, so they themselves could be VTS plugins and interact with VTube Studio directly. To interact with the VTS API (or at least with the item-related endpoints), the Web Item will need to know its own item instance UUID used to identify it inside of VTS.

To get that ID, you can use the following javascript. This will pass you the item UUID once the website has fully loaded inside of the Web Item in VTS. You can then use that ID to do stuff like move the item around, pin/unpin it, delete it (thus also closing the API connection since the browser process is shutting down) and more.

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
         }
      </script>
   </body>
</html>

```