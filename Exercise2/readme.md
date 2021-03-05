# Exercise 1 - Connect to Google drive with Open Connectors

What are we doing now and why?  As a first step we need to establish a connection between our Google Drive instance and Open Connectors to create the API documentation that we need later in Business Application Studio.  



## Open the Integration Suite from your SAP Business Technology Platform Cockpit:

(1) From your subaccount, choose **Instances and Subscriptions**.      
(2) scroll down to subscriptions and click on the **icon** right behind **Integration Suite**.   


![alt text](/Exercise2/OpenIntegrationSuite.png "OpenIntegrationSuite")   


> Alternatively click on the row and in the panes that opens to the right click on **Go to Application***   

![alt text](/Exercise2/OpenIntegrationSuiteAlt.png "OpenIntegrationSuiteAlt")


(3) A new tab will open up and within your **Integration Suite Cockpit** you will find the capability to **extend Non-SAP Connectivity** – namely the _Open Connectors_. Click to open.

> Alternatively choose Manage Capabilities and Select **Non-SAP Connectivity**.

![alt text](/Exercise2/OpenNonSAPIntegration.png "OpenNonSAPIntegration")

(4) Within **Open Connectors** click on **Connectors**.

![alt text](/Exercise2/Connectors.png "Connectors")

(5) You accessed now your Open Connector Trial through Integration Suite.



## Connect to Google Drive

(6) Browse in the **connectors** and choose **“Google Drive”** from the catalogue. When hovering over the connector select **“Authenticate”**:

![alt text](/Exercise2/GoogleDrive.png "GoogleDrive")

(7) In this new screen enter a **Connection Name** and click on **Create Instance**

![alt text](/Exercise2/CreateInstance.png "CreateInstance")


(8) You will now be **forwarded to Google to authenticate yourself**. Enter the credentials of your Google Drive account that you want to connect to.

![alt text](/Exercise2/AuthenticateGoogle.png "AuthenticateGoogle")


(9) If the authentication worked out, **you will receive a success message** as seen below in screenshot:

![alt text](/Exercise2/SuccessFullConnection.png "SuccessFullConnection")



## Invoke the Folder Contents API

(10) Go this instance by clicking on **Test in the API docs** of your created Google Drive instance.
Choose **folders** and select entry **Get** **/ folders/contents**.

![alt text](/Exercise2/InvokeFolderContents.png "InvokeFolderContents")

(11) Click **Try it out** to edit the parameters.

![alt text](/Exercise2/TryOut.png "TryOut")

(12) Fill in the **path** to your Google Drive folder that you want to connect to. In our case **/SAP**.    

**Execute** the request.

![alt text](/Exercise2/Execute.png "Execute")


(13) Verify that you see **code 200** in the response body. This means that the request was successful.

The Curl includes all the information (Request URL and parameters) that you need for connecting later in Business Application Studio towards Google Drive. In the response body itself you should now see the files and the linked metadata towards your Google Drive instance within the folder “/SAP”

![alt text](/Exercise2/Response.png "Response")



## Summary
For now this is all we need to do on Open Connectors side. Now you will see how we use these API information to create a new UI Integration Cards that connects live to Google Drive.

[Continue to Exercise 2](/Exercise3/readme.md)      
[Go back to Exercise overview](/readme.md)
