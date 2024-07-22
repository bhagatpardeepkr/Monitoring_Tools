
Well done, team! Your effort and teamwork led to the successful completion of this task. Let's keep up the good work as each step contributes to our progress. Thank you all for your hard work!









Our CD tools team doesn't raise any Jira issues for the Network team. Therefore, please raise the Jira issue with the Network Engineering team. If they require any assistance or details from us, we will be more than happy to help

After checking, I noticed that the data is not available on Graphite as well. This is the reason why data is not appearing on the Grafana dashboard after July 17. Please refer to the screenshot below for reference.

Since the CD tools team does not provide support for Telegraf and the Graphite database, I would suggest raising a Jira ticket with the Network Engineering team.





Incorrect Configuration: This is one of the most common issues. If the Dynatrace OneAgent is not properly installed or configured on your servers, it may not be able to monitor your applications and services effectively.

Networking Issues: If your servers are behind a firewall, or if there are any network connectivity issues between your servers and Dynatrace, it may prevent the OneAgent from sending monitoring data to Dynatrace.

Permission Issues: The OneAgent needs certain permissions to be able to monitor applications and services. If it doesn't have the necessary permissions, you will not be able to see the services in Dynatrace.

Unsupported Technology: Dynatrace supports multiple technologies for application and service monitoring. If your applications/services are built on a technology not supported by Dynatrace, it won't be able to monitor them.

Application Inactivity: If an application/service hasn't generated any load for a certain time period, it will not appear in the Dynatrace interface.
