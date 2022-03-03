# uofi_urb_template_APP
Description : Template to create new apps for Splunk Cloud

Download this repo, unzip it, then place the `uofi_urb_template_APP` folder in a locally running Splunk instance, ie `%SPLUNK_HOME%\etc\apps\uofi_urb_template_APP`

Rename the folder to the `<APP NAME>` you want utilizing the App Naming Convention found here : https://wiki.illinois.edu/wiki/display/splunk/Naming+Conventions#NamingConventions-CustomApps

Edit `\<APP NAME>\default\app.conf` by changing the following information :
```     
[launcher]
description = <YOUR DESCRIPTION OF THE APP>
version = <APP VERSION NUMBER>

[package]
id = <APP NAME>
      
[ui]
label = <DISPLAYED NAME OF APP IN SPLUNK>
```
Edit `\<APP NAME>\app.manifest` by changing the following information, it will need to be the same as in `app.conf` :
```
... 
"title": <DISPLAYED NAME OF APP IN SPLUNK>,
	"id": {
		"group": null,
   		"name": <APP NAME>,
   		"version": <APP VERSION NUMBER>
   	},
...
"description": <YOUR DESCRIPTION OF THE APP>,
...
```
Optional Steps :

- Change the icons or logos in `\<APP NAME>\static\`
- Add scripts `\<APP NAME>\bin\`
- Add .conf files to `\<APP NAME>\default\`
- Add lookup files to `\<APP NAME>\lookups`

Once all the changes are made, create a new branch under main in GitHub with `<APP NAME>` as the name and continue working there

Click on the `uofi_urb_template_APP` folder and at the `...` menu select `Delete directory` & commit

Click `Add file` then `Upload files` and then drag/drop `%SPLUNK_HOME%\etc\apps\<APP NAME>` & commit
	
In this branched `README.md`, replace every instance of `<APP NAME>` below with this new branch's app name and fill out details

Delete everything above & including this line & commit

# <APP NAME>
## Details
Description : 

Version : 

## Updating & Deploying
To update this app, make all changes and additions in this GitHub repo.

Once done, download this folder and add it to a locally running Splunk instance, `%SPLUNK_HOME%\etc\apps\<APP NAME>`

Run the following at the CLI in the `%SPLUNK_HOME%\bin` directory :
```
splunk package app <APP NAME>
```  
The app will be saved to `%SPLUNK_HOME%\etc\system\static\app-packages\<APP NAME>.spl`

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"
    
Log in with your https://www.splunk.com credentials & drag/drop `<APP NAME>.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
