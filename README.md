# AAA_uofi_urb_splunkmgmt_APP
App for Splunk Cloud .conf changes

Download this folder and add it to a locally running Splunk instance, %SPLUNK_HOME%\etc\apps\AAA_uofi_urb_splunkmgmt_APP

From %SPLUNK_HOME%\bin run the following at the CLI

     > splunk package app AAA_uofi_urb_splunkmgmt_AP

The file will be saved to %SPLUNK_HOME%\etc\system\static\app-packages\AAA_uofi_urb_splunkmgmt_APP.spl and will automatically have all the proper permissions assigned to all the package so it can be uploaded to Splunk Cloud without issue
 
Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"

Log in with your www.splunk.com creadentials & drag/drop the created .spl package to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
