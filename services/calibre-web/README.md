Default password: admin/admin123

## set up -  Inital 
1. follow calibre start isntructions
2. Docker compse up
3. Navigate to port 8083
4. Connect to database in data folder (should be the same one as from calibre) 

## Steps to set up kobo sync 

Config
1. Calibre-web -> Admin -> Edit Basic Configuration -> Feature Configuration
2. Check the box for "Enable Kobo Sync" and "Proxy unknown requests to Kobo Store".
3. Ensure the "Server External Port" matches Calibre Web's port (default 8083).

User Settings
1. Go to your user's settings menu (click Admin -> Edit Users).
2. Check "Sync only books in selected shelves with Kobo".
3. Click "Create/View" under the "Kobo Sync Token" section to generate an API URL.

On Kobo Device
1. open Kobo/eReader.conf
2. Edit api_endpoint=[[To the Kobo Sync Token Above]]

Debug tips. 
When adding a shelf select the sync to kobo option. if the option does not exist check to see if the user has the syncing kobo option enabled

If your Kobo device cannot change the API natively in the GUI, you'll need to follow the instructions here: 
https://jccpalmer.com/posts/setting-up-kobo-sync-with-calibre-web/