# How safe is VNet?

> If you're a security researcher and have found any vulnerabilities, please contact me at **support at denchisoft dot com** ❤️

In general, if you don't trust the other collab participants you should not use this, as they could use specialized software to steal your model during collabs. This is true for VNet and any other collab application that shares your models with other participants. People outside the collab cannot steal your model.

VNet is just one more tool you can use in your collabs. In many cases, using video-sharing-based tools like [VDO.Ninja](https://vdo.ninja/), [Discord](https://discord.com/), [ping.gg](https://ping.gg/) or [MultiV](https://iv.gg/multiv/login) is the right choice.


**Short version:**
* People outside the collab will not be able to access your files. Even if they could, all files are strongly encrypted.
* The 4 collab participants could use specialized tools to extract model and item files from memory while the collab is ongoing.
* Never use this with people you don't trust. Use video-based collab tools in that case.
* I (developer) also do not have access to any of the encryption keys so I can't decrypt any files shared during collabs. I also cannot see who is currently in a collab or any Steam IDs.


**More detailed version:**
* A host has to create a collab session. The host has to manually add up to 3 participants to the session (4 participants can be in a session), selected from their Steam friends. The host also has to set a secure session password.
* When you join a session and are not on the guest list or have the wrong password, your connection will be rejected. That means that even people who have the password cannot join without being invited by the host.
* No new participants can be added to the guest list while the session is ongoing.
* When you join a session with the correct password and you are on the guest list, you will be presented with a list of all other invited participants and can choose whether or not you want to actually enter the session.
* If you choose to join the session, any items/models you load will be uploaded to the VNet servers. Before the upload, they are encrypted with a 256 bit AES key. The file name for the upload will also be randomized (random 32 byte hex string)
* The encryption key and random file name are then distributed to all connected session participants. The key and file name are never shown or stored by VTS so you cannot accidentally reveal anything on stream.
* The other participants will download all shared files and decrypt/load them automatically. The files (including Live2D models) will be loaded entirely from memory and are never stored on the other participants' PCs.
* When the host closes the session, all files that were shared during the session are deleted from the VNet servers.
* If for some reason the host's VTube Studio crashes, it won't be able to delete the files anymore since the random filenames are never stored locally. Any files left on the VNet servers will automatically be wiped after 24 hours (max. session time).


Super detailed version (this will also be published): https://denchisoft.com/wp-content/uploads/2023/04/vnet_setup_v1.pdf





[VNet Sequence Diagram and Security Details](https://denchisoft.com/wp-content/uploads/2023/04/vnet_setup_v1.pdf)

