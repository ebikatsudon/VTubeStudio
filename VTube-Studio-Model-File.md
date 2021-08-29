## VTube Studio Models

All files VTube Studio generates to save your model setup and meta data are fully human-readable, not encrypted and use a JSON format.

Currently, VTube Studio saves all model-related configuration data in a file right next to your Live2D model. The file is called:

**\<Your-Live2D-Model-Name\>.vtube.json**

There is no documentation available for the file format at this point, but if you’re interested, just open them up in your favorite text editor. Most things should be relatively self-explanatory. But please be advised that manipulating your model fines manually may result in broken files so please be careful.

## Auto-backups

When you modify any model settings in VTube Studio, the model file is automatically saved instantly. Also, VTube Studio checks every 5 minutes if the currently loaded model was modified and if it was, it saves a safety-copy into the `"Backups"` folder next to the `"Live2DModels"` folder.