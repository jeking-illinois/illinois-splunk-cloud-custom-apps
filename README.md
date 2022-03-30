# uofi_ua_ghss_aits
## Details
Description : GitHub Shared Service for the Univeristy of Illinois System

Version : 1.0.0

## Updating & Deploying
To update this app, make all changes and additions in this GitHub repo.

The miminum requirement will be to change the version information in this `README.md` file and also in the `uofi_ua_ghss_AITS/default/app.conf` file

Once done, download this folder and add it to a locally running Splunk instance, `%SPLUNK_HOME%/etc/apps/uofi_ua_ghss_AITS`

Run the following at the CLI in the `%SPLUNK_HOME%/bin` directory :
```
splunk package app uofi_ua_ghss_AITS
```  
The app will be saved to `%SPLUNK_HOME%/etc/system/static/app-packages/uofi_ua_ghss_AITS.spl`

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"
    
Log in with your https://www.splunk.com credentials & drag/drop `uofi_ua_ghss_AITS.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
