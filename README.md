# TA-crowdstrike-falcon-data-replicator--sqs
## Details
Description : "Sidecar" app for the official "CrowdStrike Falcon Data Replicator SQS" version 2.2.0

Version : 1.0.0

## Updating & Deploying
To update this app, make all changes and additions in this GitHub repo.

Once done, download this folder and add it to a locally running Splunk instance, `%SPLUNK_HOME%\etc\apps\TA-crowdstrike-falcon-data-replicator--sqs`

Run the following at the CLI in the `%SPLUNK_HOME%\bin` directory :
```
splunk package app TA-crowdstrike-falcon-data-replicator--sqs
```  
The app will be saved to `%SPLUNK_HOME%\etc\system\static\app-packages\TA-crowdstrike-falcon-data-replicator--sqs.spl`

Navigate to https://illinois.splunkcloud.com/en-US/app/dmc/uploaded_apps and click "Upload App"
    
Log in with your https://www.splunk.com credentials & drag/drop `TA-crowdstrike-falcon-data-replicator--sqs.spl` into the Web interface to begin the App Validation process

Once done you will be notified if the app is accepted & ready to install or rejected with a report detailing the reasons

Installing apps initiates a Search Head Cluster restart
