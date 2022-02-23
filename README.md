# Splunk_TA_tomcat_CUSTOM
## Details
Description : Splunk Add-on for Tomcat - CUSTOM application removing unneeded sections including Log4j vulnerabilities

Version : 1.1.1

## Updating & Deploying
To update this app, make all changes and additions in this GitHub repo.

Once done, download this folder and add it to a locally running Splunk instance, `%SPLUNK_HOME%\etc\apps\Splunk_TA_tomcat_CUSTOM`

Run the following at the CLI in the `%SPLUNK_HOME%\bin` directory :
```
splunk package app Splunk_TA_tomcat_CUSTOM
```  
The app will be saved to `%SPLUNK_HOME%\etc\system\static\app-packages\Splunk_TA_tomcat_CUSTOM.spl`

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"
    
Log in with your https://www.splunk.com creadentials & drag/drop `Splunk_TA_tomcat_CUSTOM.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
