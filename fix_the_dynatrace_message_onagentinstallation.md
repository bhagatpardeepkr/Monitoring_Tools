##   How to install the oneagent on the kubernetes node and fix the dynatrace message


How to install the oneagent on the kubernetes node and fix the dynatrace message
A guide for resolving the issue of not fully monitored kubernetes nodes in dynatrace
Introduction
Dynatrace is a software intelligence platform that provides full-stack monitoring and observability for cloud-native applications. Dynatrace uses a lightweight agent called oneagent to collect data from the host and the processes running on it. Oneagent can be installed on various types of hosts, including kubernetes nodes.
However, sometimes dynatrace may show a message that some of the kubernetes nodes are not fully monitored and suggest to install the oneagent on the kubernetes node to get full visibility. This message may appear on all pods in dynatrace, even if the oneagent is already installed on the node. This document will explain the reason of this message and how to install the oneagent on the kubernetes node to get full visibility.
Reason of the message
The reason of getting the same message on all pods in dynatrace is that dynatrace does not detect the oneagent installation on the kubernetes node automatically. Dynatrace relies on a label called oneagent.dynatrace.com/install to identify the nodes that have the oneagent installed. If this label is missing or set to false, dynatrace will assume that the node is not fully monitored and show the message on all pods running on that node.
This label can be missing or set to false for various reasons, such as:
•	The oneagent was installed manually on the node, without using the dynatrace operator or the helm chart.
•	The oneagent was installed using the dynatrace operator or the helm chart, but the label was not applied or was removed later.
•	The oneagent was installed using the dynatrace operator or the helm chart, but the installation failed or was incomplete.
•	The oneagent was uninstalled from the node, but the label was not removed.
To verify if the oneagent is installed on the node, you can use the following command:
kubectl get pods -n dynatrace -o wide
This command will show the pods in the dynatrace namespace and the nodes they are running on. If you see a pod with the name oneagent-* on the node, it means that the oneagent is installed on that node. If you don't see such a pod, it means that the oneagent is not installed on that node.
How to install the oneagent on the kubernetes node
The recommended way to install the oneagent on the kubernetes node is to use the dynatrace operator or the helm chart. These methods will ensure that the oneagent is installed correctly and that the label is applied to the node. The steps to install the oneagent using these methods are as follows:
Using the dynatrace operator
The dynatrace operator is a kubernetes custom resource that automates the deployment and management of the oneagent. To install the oneagent using the dynatrace operator, you need to do the following:
•	Create a dynatrace namespace if it does not exist.
•	Install the dynatrace operator using the kubectl command or the web console.
•	Create a oneagent custom resource with the required parameters, such as the dynatrace API URL, the API token, and the node selector.
•	Apply the oneagent custom resource to the cluster.
•	Wait for the oneagent pods to be created and running on the selected nodes.
•	Verify that the label oneagent.dynatrace.com/install is set to true on the nodes.
For more details on how to install the oneagent using the dynatrace operator, please refer to the official documentation: [URL]
Using the helm chart
The helm chart is a package that contains the configuration and templates for deploying the oneagent on kubernetes. To install the oneagent using the helm chart, you need to do the following:
•	Add the dynatrace helm repository to your helm client.
•	Update the helm repository index.
•	Create a values.yaml file with the required parameters, such as the dynatrace API URL, the API token, and the node selector.
•	Install the oneagent helm chart using the helm install command.
•	Wait for the oneagent pods to be created and running on the selected nodes.
•	Verify that the label oneagent.dynatrace.com/install is set to true on the nodes.
For more details on how to install the oneagent using the helm chart, please refer to the official documentation: [URL]
Conclusion
In this document, we have explained the reason of getting the same message on all pods in dynatrace that some of the kubernetes nodes are not fully monitored and how to install the oneagent on the kubernetes node to get full visibility. We have also shown how to verify if the oneagent is installed on the node and how to use the dynatrace operator or the helm chart to install the oneagent correctly and apply the label to the node. By following these steps, you should be able to resolve the issue and get full visibility of your kubernetes nodes in dynatrace.

