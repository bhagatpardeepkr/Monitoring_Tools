How to Change Dynatrace Dashboard Ownership in the JSON File
Changing the ownership of a Dynatrace dashboard is necessary when the original owner has left the organization or is no longer part of the team managing it. This knowledge base article provides a step-by-step guide on how to change dashboard ownership in Dynatrace via modifications in the dashboard’s JSON configuration file. This method serves as a temporary fix until permanent functionality or user management integration is facilitated in Dynatrace.

Prerequisites
Access rights to modify and manage dashboards in Dynatrace.
Access to the JSON configuration file for the dashboard.
Basic understanding of JSON file structures.
Steps to Change Dashboard Owner
Step 1: Export Current Dashboard Configuration
Login into the Dynatrace web interface.
Navigate to the dashboard you wish to change ownership of.
On the dashboard, go to Settings (usually found as a cogwheel icon).
Select Dashboard JSON from the dropdown options.
Click on the Export button. A JSON file containing the dashboard’s configuration will be downloaded to your system.
Step 2: Modify the JSON File
Open the downloaded JSON file with a text editor capable of handling JSON syntax, such as Notepad++, Visual Studio Code, or any IDE of your choice.
Locate the "owner" property in the JSON. This can generally be found near the top of the file and may look something like:
json


"owner": "old.owner@company.com",
Replace the existing email address or owner identifier with the new owner’s email or identifier:
json


"owner": "new.owner@company.com",
Save the changes to the file. Ensure that the file maintains its JSON format.
Step 3: Import the Modified Dashboard Configuration
Return to the Dynatrace dashboard web interface where the original dashboard is located.
Go to Settings > Dashboard JSON.
This time, click Import.
Browse and select the modified JSON file from your computer and import it.
The dashboard should now reflect the new owner’s details. Confirm by revisiting the dashboard settings.
Important Notes
Use this method as a temporary fix. For organizations with strict user rights and data governance policies, verify compliance before changing dashboard ownership.
Keep a backup of the original JSON file before modifying it. In case of any issues, you may revert to the original configuration.
Ensure that the new owner has the proper authorization levels required to access and manage the dashboard.
Conclusion
Changing the owner of a Dynatrace dashboard through JSON file modifications is straightforward but must be handled carefully to ensure data integrity and compliance with enterprise policies. For a more permanent solution or to automate this process, consider consulting Dynatrace’s administration options or API features that might allow more dynamic user management.

For further assistance, please contact your Dynatrace administrator or support team.
