As a Dynatrace admin, to dig deep into an issue, you can ask the user to provide the following information:

From your document

Detailed Description of the Issue: Ask the user to provide a detailed description of the issue they are experiencing, including any error messages or unusual behavior they have observed1.
Screenshots or Images: Request screenshots or images that show the issue, as these can help in understanding the problem better1.
Time Frame: Ask for the specific time frame during which the issue occurred. This can help in correlating the issue with any events or changes that might have happened during that period1.
Environment Details: Request information about the environment where the issue is occurring, such as the type of servers, operating systems, and any relevant configurations1.
Steps to Reproduce: Ask the user to provide the steps they took that led to the issue. This can help in reproducing the problem and identifying its root cause1.
Logs and Metrics: Request relevant logs and metrics from Dynatrace or other monitoring tools. This can provide valuable insights into what might be causing the issue1.


Data inconsistency between different data sources: Dynatrace collects data from various sources, such as agents, integrations, logs, and synthetic tests. Some of these sources may have different data retention policies, data processing delays, or data quality issues, leading to inconsistent data loading.
Data caching and refreshing issues: Dynatrace uses caching mechanisms to improve performance and scalability. However, caching could introduce data inconsistency if the cache is not refreshed or invalidated properly, or if there are network or server issues preventing the cache from being updated.
Data aggregation and sampling issues: Dynatrace aggregates and samples data to reduce data volume and complexity. Aggregation and sampling could introduce data inconsistency if the methods are not consistent, or if there are data outliers or anomalies affecting the results.
