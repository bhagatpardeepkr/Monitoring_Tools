Kubernetes cluster filter
The Kubernetes cluster filter is a built-in filter that is available in the Dynatrace UI. It allows users to select one or more Kubernetes clusters from a drop-down list and view the data and metrics of the selected clusters. The Kubernetes cluster filter can be applied to various dashboards, charts, and reports in Dynatrace. For example, users can use the Kubernetes cluster filter to view the cluster overview, the cluster health, the cluster events, the cluster nodes, the cluster pods, the cluster services, and the cluster namespaces.

K8s cluster name filter tag

The K8s cluster name filter tag is a custom filter tag that is created by the user. It allows users to assign a name to a Kubernetes cluster and use it as a filter criterion. The K8s cluster name filter tag can be applied to any entity that is related to the Kubernetes cluster, such as hosts, processes, services, applications, and custom devices. For example, users can use the K8s cluster name filter tag to view the performance, availability, and dependencies of the services that are running on a specific Kubernetes cluster.


Difference between the two filters

•	The Kubernetes cluster filter is a built-in filter that is available in the Dynatrace UI, while the K8s cluster name filter tag is a custom filter tag that is created by the user.

•	The Kubernetes cluster filter can only be applied to the data and metrics of Kubernetes clusters, while the K8s cluster name filter tag can be applied to any entity that is related to the Kubernetes cluster.

•	The Kubernetes cluster filter can only select one or more Kubernetes clusters from a drop-down list, while the K8s cluster name filter tag can assign any name to a Kubernetes cluster and use it as a filter criterion.

•	The Kubernetes cluster filter can be used to view the cluster-level information, such as the cluster overview, the cluster health, the cluster events, the cluster nodes, the cluster pods, the cluster services, and the cluster namespaces, while the K8s cluster name filter tag can be used to view the entity-level information, such as the performance, availability, and dependencies of the services that are running on a specific Kubernetes cluster.










































The reason of getting the same message on all pods in dynatrace is that dynatrace does not detect the oneagent installation on the kubernetes node automatically. Dynatrace relies on a label called oneagent.dynatrace.com/install to identify the nodes that have the oneagent installed. If this label is missing or set to false, dynatrace will assume that the node is not fully monitored and show the message on all pods running on that node

kubectl describe pod <pod-name> -n <namespace-name>

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
