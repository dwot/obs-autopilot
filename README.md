# obs-autopilot
Prototype AutoPilot script for OBS, interweaving video playlists.

## PreReqs
1. 2 Playlists in M3U format w/ absolute file paths
 * 1st File is Main playlist of programs to be played in order
 * 2nd File is Inserts playlist of bumps / commercials / prerolls to be played in between items in main playlist
2. OBS Studio installed and running
3. VLC installed and running
4. VLC Source plugin for OBS Studio detecting VLC properly
5. 2 Scenes setup in OBS each with a VLC Source
6. OBS Websockets plugin installed, running properly and available on a port
  
## Steps
1. Load AutoPilot Tool - https://dwot.github.io/obs-autopilot/websocket.html
2. Select M3U playlist for Inserts
* Parsed entries and duration in seconds should display
3. Select M3U playlist for Main Program
* Parsed entries and duration in seconds should display
4. Enter Scene and Source names for 2 VLC scenes / sources established in OBS in PreReqs
5. Enter IP & Port of OBS Websocket plugin and hit connect
* As each entry in mains playlist is completed, the next entry in inserts playlist will be loaded and played.
* When the insert item has completed the next item in the mains playlist will be loaded and played.
