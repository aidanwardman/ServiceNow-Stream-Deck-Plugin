# Stream Deck ServiceNow Plugin
## Preview
![ServiceNow Stream Deck Preview](preview.PNG)
## Features
- Track all major ticket types from your ServiceNow instance
- Individually configurable counters (Ticket Type / Active State / Time Period)
- Global Settings override for fast alternate views (Toggle On to apply global settings to all counters, Toggle Off to revert counters to individually configured state)
- One time, reusable instance configuration action to apply settings to all buttons/actions
## Requirements
- A Stream Deck by Elgato is required to use this plugin
- The JSONP Wrapper included in this repository is required to be installed on your instance for this plugin to work
### JSONP Wrapper Installation
1. In your ServiceNow instance, create a new UI Page with the name **jsonp**
2. In the **HTML** field of the UI Page, paste the contents of the file **jsonp** (included in this repository)
3. In the application navigator filter of your instance, type **sys_public.list**
4. Click **New**
5. In the **sys_public** table, create a record with the following values
   - **Page** : jsonp 
   - **Active** : Ticked / Checked

Instructions on how to make a page public in your instance can also be found at [Making a Page Public](http://wiki.servicenow.com/index.php?title=Making_a_Page_Public)
### Usage
1. Setup the jsonp wrapper on your ServiceNow instance using the instructions above.
2. Download the plugin "com.aidanwardman.snow.streamDeckPlugin".
3. Install the plugin by double clicking the plugin file. You may wish to accept the installation of the provided profile to save time.
4. Click on the Configuration Tool "Remove Me After Config" (note, if you use the included profile this will not be removable).
5. Enter your instance URL (with out trailing /), username and password, click apply, the icon should turn into a green tick.
6. For each Live Counter "CONFIG Required", click on it, select what you would like it to display, then click apply.
7. The "Active State" and "Time Period" buttons are toggle buttons, to apply their values("filters") to all buttons click the "Global Settings" button to "On". Click "Global Settings" again to revert all Live Counters to their set value.