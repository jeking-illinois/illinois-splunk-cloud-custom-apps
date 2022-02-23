# uofi_urb_template_APP
Template to create new apps for Splunk Cloud.

Download this folder and place it in a locally running Splunk instance, %SPLUNK_HOME%\etc\apps\uofi_urb_template_APP 

Rename the folder to the <APP NAME> yong the App Naming Convention found here : https://wiki.illinois.edu/wiki/display/splunk/Naming+Conventions#NamingConventions-CustomApps

First edit <APP NAME>\default\app.conf by changing the following basic information:
      [launcher]
      description = <YOUR DESCRIPTION>
  
      [package]
      id = <APP NAME>
  change the icons or logos in %SPLUNK_HOME%\etc\apps\<APP NAME>_APP\static\, and add any additional scripts or KOs to %SPLUNK_HOME%\etc\apps\<APP NAME>_APP\bin\ or %SPLUNK_HOME%\etc\apps\<APP NAME>_APP\default\
  
  Back in %SPLUNK_HOME%\ run the following at the CLI

     > splunk package app <APP NAME>_APP

  The file will be saved to %SPLUNK_HOME%\etc\system\static\app-packages\<APP NAME>_APP.spl and will automatically have all the proper permissions assigned to all the package so it can be uploaded to Splunk Cloud without issue.


App for Splunk Cloud .conf changes

Download this folder and add it to a locally running Splunk instance, %SPLUNK_HOME%\etc\apps\AAA_uofi_urb_splunkmgmt_APP

From %SPLUNK_HOME%\bin run the following at the CLI

 > splunk package app AAA_uofi_urb_splunkmgmt_AP
The file will be saved to %SPLUNK_HOME%\etc\system\static\app-packages\AAA_uofi_urb_splunkmgmt_APP.spl and will automatically have all the proper permissions assigned to all the package so it can be uploaded to Splunk Cloud without issue

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"

Log in with your www.splunk.com creadentials & drag/drop the created .spl package to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
