# Exercise 2 - Connect to Google drive with Open Connectors

What are we doing now and why?  As a first step we need to establish a connection between our Google Drive instance and Open Connectors to create the API documentation that we need later in Business Application Studio.  

## Open the Integration Suite from your SAP Business Technology Platform Cockpit:

From your subaccount, choose **Instances and Subscriptions**.   
scroll down to subscriptions and click on the **icon** right behind **Integration Suite**.   


![alt text](/Exercise2/OpenIntegrationSuite.png "OpenIntegrationSuite")   


> Alternatively click on the row and in the panes that opens to the right click on **Go to Application***   

![alt text](/Exercise2/OpenIntegrationSuiteAlt.png "OpenIntegrationSuiteAlt")


Within your Integration Suite Cockpit you will find the capability to **extend Non-SAP Connectivity** – namely the _Open Connectors_:   
![alt text](/Exercise2/OpenNonSAPIntegration.png "OpenNonSAPIntegration")

![alt text](/Exercise2/Connectors.png "Connectors")

You accessed now your Open Connector Trial through Integration Suite.

## Connect to Google Drive

Browse in the connectors and choose “Google Drive” from the catalogue. When hovering over the connector select “Authenticate”:
![alt text](/Exercise2/GoogleDrive.png "GoogleDrive")

![alt text](/Exercise2/CreateInstance.png "CreateInstance")

Enter the credentials of your Google Drive account that you want to connect to:
![alt text](/Exercise2/AuthenticateGoogle.png "AuthenticateGoogle")

If the authentication worked out, you will receive a success message as seen below in screenshot:

![alt text](/Exercise2/SuccessFullConnection.png "SuccessFullConnection")

## Invoke the Folder Contents API

Go to instances and to the API Docs of your created Google Drive instance:
Choose “folders” -> “Get” / folders / contents:
![alt text](/Exercise2/InvokeFolderContents.png "InvokeFolderContents")

Click “Try it out” to edit the parameters:

![alt text](/Exercise2/TryOut.png "TryOut")

Fill in the path to your Google Drive folder that you want to connect to. In our case /SAP. Execute the request.
![alt text](/Exercise2/Execute.png "Execute")


The Curl includes all the information (Request URL and parameters) that you need for connecting later in Business Application Studio towards Google Drive. You see in the response body by the code 200, that the request was successful. In the response body itself you should now see the files and the linked metadata towards your Google Drive instance within the folder “/SAP”
![alt text](/Exercise2/Response.png "Response")

## Summary
For now this is all we need to do on Open Connectors side. Now you will see how we use these API information to create a new UI Integration Cards that connects live to Google Drive.

[Continue to Exercise 3](/Exercise3/readme.md)      
[Go back to Exercise overview](/readme.md)
