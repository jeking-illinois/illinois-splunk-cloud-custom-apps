# AAA_uofi_urb_splunkmgmt_APP
## Details
Description : App for Splunk Cloud .conf changes

Version : 1.0.3


## Updating & Deploying
To update this app, make all changes and additions in this GitHub repo.

The miminum requirement will be to change the version information in this `README.md` file and also in the `<APP NAME>/default/app.conf` file

Once done, download this folder and add it to a locally running Splunk instance, `%SPLUNK_HOME%/etc/apps/AAA_uofi_urb_splunkmgmt_APP`

Run the following at the CLI in the `%SPLUNK_HOME%/bin` directory :
```
splunk package app AAA_uofi_urb_splunkmgmt_APP
```  
The app will be saved to `%SPLUNK_HOME%/etc/system/static/app-packages/AAA_uofi_urb_splunkmgmt_APP.spl`
 
Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"

Log in with your https://www.splunk.com credentials & drag/drop `AAA_uofi_urb_splunkmgmt_APP.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
