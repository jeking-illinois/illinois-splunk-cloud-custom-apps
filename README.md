# uofi_urb_template_APP
Description : Template to create new apps for Splunk Cloud.

The only required step is to edit `\<APP NAME>\default\app.conf` by changing the following basic information :
```     
[launcher]
description = <YOUR DESCRIPTION>

[package]
id = <APP NAME>
      
[ui]
label = <DISPLAYED NAME OF APP IN SPLUNK>
```
Optional Steps :

- Change the icons or logos in \<APP NAME>\static\
- Add scripts \<APP NAME>\bin\
- Add .conf files to \<APP NAME>\default\
- If including lookups, create a folder \<APP NAME>\lookups and add them there

      
In the new branch, delete everything above & including this line in the README.md and replace <APP NAME> with the new app's name
      
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

Log in with your https://www.splunk.com creadentials & drag/drop `<APP NAME>.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
