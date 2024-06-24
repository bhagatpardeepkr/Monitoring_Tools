

systemctl status fits-mq-metrics-collector. 

Steps to follow
•	Step 1: Verify the data source connection
The first step is to check if the data source that feeds the data to the Grafana dashboard is connected and working properly. You can do this by going to the data source settings in Grafana and clicking on the "Test" button. If the connection is successful, you will see a green message saying "Data source is working". If the connection fails, you will see a red message with an error code and a possible reason for the failure. You can then try to fix the connection issue by following the suggestions in the error message or contacting the data source provider.
•	Step 2: Check the data source query
The next step is to check if the data source query that fetches the data from the data source is correct and valid. You can do this by going to the panel settings in Grafana and clicking on the "Query inspector" button. This will show you the query that is sent to the data source and the response that is received. You can then compare the query and the response with the expected results and see if there are any discrepancies or errors. You can also try to modify the query parameters or filters and see if the response changes accordingly. If the query is incorrect or invalid, you can correct it by following the query syntax and documentation of the data source.
•	Step 3: Refresh the dashboard
•	The final step is to refresh the dashboard and see if the data is updated and displayed correctly. You can do this by clicking on the "Refresh dashboard" button in Grafana or by setting a refresh interval in the dashboard settings. If the data is still not feeding into the dashboard, you may need to clear the browser cache or restart the Grafana server. If the problem persists, you can contact the Grafana support team or the data source provider for further assistance.





















Search: Start with a search that defines the event you want to be alerted about. Run a search query in the search bar to find the event you're interested in.

Save As Alert: Once your search is showing the results you want to trigger an alert for, click the 'Save As' button above the search results, and then click 'Alert'.

Configure Alert: A dialog box will open, allowing you to set the various options for the alert. Here you can specify the alert type (real-time or scheduled), trigger conditions (like number of results, specific values, etc.), throttling options (to limit retriggering of alerts), and actions (like send email, run script, etc.).

Save: Once you've configured the alert options as needed, click 'Save' to create the alert.















Aks access
Grafana access in cyberark
Github access



# ROUND((B1-A1)*24*60,0)


Solution for the Interested Party Document failure alert
The Interested Party Document is a document that allows the account owner or an eligible signer to share their account information with a third party, such as a CPA. To generate this document, several services are involved, such as GNA Accounts Service, Contacts REST, EngageOne, Printer Services, and E-sign Services. Sometimes, the document generation may fail due to various reasons, such as incomplete or missing data, service outages, printing or e-sign errors, etc. In this case, an alert should be triggered to notify the relevant team or person to investigate and resolve the issue.
To create an alert for the Interested Party Document failure, the following steps are suggested:
•	Use the Splunk query that you have created to filter out the exceptions that are due to missing data, as these are not directly related to the document generation process. You can also exclude any other exceptions that are not relevant or actionable for the alert.
•	Set a threshold for the alert based on the frequency and severity of the document failure. For example, you can set the alert to trigger when the number of document failures exceeds 10 per hour, or when the failure rate is higher than 10% of the total document requests.
•	Define the alert message and the notification channel. The alert message should include the following information: the number and percentage of document failures, the time range of the alert, the possible causes of the failure, and the steps to take to fix the issue. The notification channel should be the one that is most convenient and effective for the alert recipient, such as email, Slack, PagerDuty, etc.
•	Test the alert and monitor its performance. You can use some test data or scenarios to trigger the alert and check if it works as expected. You can also monitor the alert frequency, accuracy, and usefulness, and adjust the alert settings as needed.
To fix the issue of the Interested Party Document failure, the following steps are suggested:
•	Identify the root cause of the failure. You can use the Splunk query and the alert message to narrow down the possible causes, such as which service is failing, what data is missing or incorrect, what error code or message is returned, etc.
•	Follow the appropriate troubleshooting steps based on the root cause. For example, if the failure is due to a service outage, you can check the service status and logs, and contact the service owner or provider. If the failure is due to a data issue, you can verify the data source and quality, and contact the data owner or provider. If the failure is due to a printing or e-sign error, you can check the printer or e-sign service settings and logs, and contact the printer or e-sign service provider.
•	Verify the fix and document the resolution. You can use some test data or scenarios to verify that the document generation works correctly after the fix. You can also document the resolution steps and results, and share them with the relevant stakeholders.
