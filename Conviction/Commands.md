### l3d-post
Toggles post processing effects on/off

### l3d-start-captureimages
Starts capturing each frame to a png. Can specify a filename (unclear what is valid) or it will default to dumping to system/CaptureImages

**Syntax:** *l3d-start-captureimages %s*

### l3d-stop-captureimages
Stops the above function

### l3d-toggle-lod
Toggles LOD quality

### l3d-toggle-ao
Toggles ambient occlusion on/off

### l3d-distance-fade
Toggles certain actors on/off in the distance

### l3d-shadows
Toggles shadows

### l3d-char-lighting
Toggles personal lights on the player and all NPCs

### freecam
Toggles freecam. Dpad up/down will change the height, while the triggers modify move speed. 

### fixcam
Toggles the camera between where you left it and on the player. Should be set with freecam first.

### open
Opens a map with optional parameters

**Syntax:** *open %s*  
**Syntax:** *open %s?params*

Optional parameters: 
- ?restart     // Fully restarts the level
- ?restartbb   // Restarts at the current blackbox? Reloads checkpoint?
- ?GameMode=   // Specify the mode
  - CoopStory
  - Hunter
  - Purestealth
  - Faceoff
  - Laststand
- ?Splitscreen // Spawns Archer and Kestrel in splitscreen config. Player 2 is not controllable.

**Example:** open C01_MafiaClub // loads St. Petersburg Banya in Hunter mode  
**Example:** open C01_MafiaClub?GameMode=CoopStory?Splitscreen // loads St. Petersburg Banya in Coop Story splitscreen
