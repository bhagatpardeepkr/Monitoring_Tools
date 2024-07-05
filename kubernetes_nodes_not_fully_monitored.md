## Troubleshooting dynatrace case for kubernetes nodes not fully monitored

Troubleshooting dynatrace case for kubernetes nodes not fully monitored
A guide for administrators to diagnose and resolve the issue of incomplete monitoring of kubernetes nodes by dynatrace
Introduction
Dynatrace is a software intelligence platform that provides full-stack monitoring and observability for cloud-native applications running on kubernetes clusters. Dynatrace uses OneAgent, a lightweight agent that runs on each kubernetes node and automatically injects into the pods to collect metrics, traces, logs, and events from the workloads.
However, sometimes dynatrace may report that some of the kubernetes nodes are not fully monitored, and an administrator have to look into the issue. This means that dynatrace is not able to inject OneAgent into some of the pods running on those nodes, and therefore cannot monitor them properly. This document will explain the possible causes and solutions for this problem, and provide a step-by-step guide for troubleshooting the issue.
Possible causes and solutions
There are several factors that may prevent dynatrace from injecting OneAgent into the pods, such as:
•	Insufficient permissions or resources for OneAgent on the kubernetes node or the pod.
•	Conflicting or incompatible configurations or settings on the kubernetes node or the pod.
•	Network or firewall issues that block the communication between OneAgent and dynatrace server or cluster.
•	Outdated or corrupted OneAgent versions or images on the kubernetes node or the pod.
The solutions for each of these factors may vary depending on the specific situation, but some general recommendations are:
•	Ensure that OneAgent has the required permissions and resources to run on the kubernetes node and the pod, such as the appropriate service account, role, role binding, daemon set, and resource limits and requests.
•	Check and adjust the configurations and settings on the kubernetes node and the pod that may affect OneAgent injection, such as the pod security policy, the container runtime, the init containers, the environment variables, the labels, and the annotations.
•	Verify and troubleshoot the network and firewall settings that may block or interfere with the communication between OneAgent and dynatrace server or cluster, such as the DNS resolution, the proxy settings, the ports, and the network policies.
•	Update and reinstall OneAgent on the kubernetes node and the pod to the latest version and image, and ensure that they are compatible with the dynatrace server or cluster version and the kubernetes version.
Troubleshooting steps
The following steps will help you to diagnose and resolve the issue of kubernetes nodes not fully monitored by dynatrace:
1.	Log in to the dynatrace web UI and navigate to the kubernetes dashboard. Identify the kubernetes nodes that are not fully monitored and the pods that are running on them.
2.	Click on the node name and check the node overview page. Look for any errors, warnings, or alerts that may indicate the cause of the problem. For example, you may see messages like "OneAgent injection failed", "OneAgent injection skipped", or "OneAgent injection disabled".
3.	Click on the pod name and check the pod overview page. Look for any errors, warnings, or alerts that may indicate the cause of the problem. For example, you may see messages like "OneAgent injection failed", "OneAgent injection skipped", or "OneAgent injection disabled".
4.	Click on the "View pod logs" button and check the logs of the OneAgent pod and the workload pod. Look for any errors, warnings, or messages that may indicate the cause of the problem. For example, you may see messages like "OneAgent injection failed", "OneAgent injection skipped", or "OneAgent injection disabled".
5.	Based on the information gathered from the previous steps, apply the appropriate solution for the identified cause of the problem. For example, you may need to modify the permissions, resources, configurations, settings, network, firewall, or OneAgent version or image on the kubernetes node or the pod.
6.	Restart the OneAgent pod and the workload pod on the affected node and check if the issue is resolved. You can use the kubectl command line tool or the dynatrace web UI to perform this action.
7.	Repeat the steps for each kubernetes node and pod that are not fully monitored by dynatrace until the issue is resolved.

