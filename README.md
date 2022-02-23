# uofi_urb_template_APP
Template to create new apps for Splunk Cloud.

Download this folder and place it in a locally running Splunk instance, %SPLUNK_HOME%\etc\apps\uofi_urb_template_APP 

Rename the folder to the <APP NAME> you want utilizing the App Naming Convention found here : https://wiki.illinois.edu/wiki/display/splunk/Naming+Conventions#NamingConventions-CustomApps

The only required step is to edit \<APP NAME>\default\app.conf by changing the following basic information :
      
      [launcher]
      description = <YOUR DESCRIPTION>
  
      [package]
      id = <APP NAME>
      
      [ui]
      label = <DISPLAYED NAME OF APP IN SPLUNK>

Optional Steps :

- Change the icons or logos in \<APP NAME>\static\
- Add scripts \<APP NAME>\bin\
- Add .conf files to \<APP NAME>\default\
- If including lookups, create a folder \<APP NAME>\lookups and add them there

Once all the additions and changes are made, run the following at the CLI in the %SPLUNK_HOME%\bin directory :

     splunk package app <APP NAME>

The app will be saved to %SPLUNK_HOME%\etc\system\static\app-packages\<APP NAME>.spl 
      This process compresses the app into a .spl file and files are granted proper "Splunk" permissions to pass App Validation

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"

Log in with your www.splunk.com creadentials & drag/drop <APP NAME>.spl into the Web interface to begin the App Validation process
      
Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
