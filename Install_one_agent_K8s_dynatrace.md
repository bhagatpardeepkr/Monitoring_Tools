## How to install and monitor dynatrace oneagent in kubernetes

How to install and monitor dynatrace oneagent in kubernetes
A guide for kubernetes administrators and developers
Introduction
Dynatrace is a software intelligence platform that provides full-stack observability and automation for cloud-native applications. Dynatrace oneagent is a single agent that automatically collects metrics, traces, logs, and events from the host and the containers running on it. Oneagent can be deployed as a daemonset on kubernetes clusters, which ensures that every node and pod is monitored by dynatrace.
This document will explain the best practices to install oneagent on kubernetes, and how to monitor the performance, availability, and health of kubernetes nodes and pods on dynatrace.
Prerequisites
Before installing oneagent on kubernetes, you need to have the following:
•	A dynatrace account with an environment ID and a PaaS token. You can find them in the Deploy dynatrace section of the dynatrace web UI.
•	A kubernetes cluster with kubectl access and administrator privileges.
•	A docker registry that is accessible from the kubernetes cluster, where you can push the oneagent image.
Installation steps
To install oneagent on kubernetes, follow these steps:
1.	Download the oneagent docker image from the dynatrace web UI. Go to Deploy dynatrace > Start installation > Linux > Download agent > Docker.
2.	Push the oneagent image to your docker registry. For example, if your registry is docker.io, use the following command:
3.	docker push docker.io/yourusername/oneagent:latest
4.	Create a secret in your kubernetes cluster that contains your dynatrace environment ID and PaaS token. For example, use the following command:
5.	kubectl create secret generic oneagent --from-literal=apiToken=YOUR_PAAS_TOKEN --from-literal=paasToken=YOUR_ENVIRONMENT_ID
6.	Download the oneagent kubernetes manifest from the dynatrace web UI. Go to Deploy dynatrace > Start installation > Kubernetes.
7.	Edit the oneagent kubernetes manifest to specify the image name and tag of your oneagent image in the docker registry. For example, change the image value to:
8.	image: docker.io/yourusername/oneagent:latest
9.	Apply the oneagent kubernetes manifest to your kubernetes cluster. For example, use the following command:
10.	kubectl apply -f dynatrace-oneagent.yml
After applying the manifest, oneagent will be deployed as a daemonset on your kubernetes cluster, and it will start monitoring your nodes and pods automatically.
Monitoring kubernetes nodes and pods on dynatrace
Once oneagent is installed on your kubernetes cluster, you can monitor the performance, availability, and health of your kubernetes nodes and pods on dynatrace. You can access the following features on the dynatrace web UI:
•	Kubernetes overview: This dashboard shows the status and metrics of your kubernetes clusters, namespaces, nodes, and pods. You can filter, sort, and drill down into the details of each entity. You can also see the topology and dependencies of your kubernetes components.
•	Kubernetes events: This dashboard shows the events that occur on your kubernetes clusters, such as node or pod creation, deletion, scaling, or failure. You can filter, sort, and drill down into the details of each event. You can also see the impact and root cause of each event.
•	Kubernetes metrics: This dashboard shows the metrics that are collected by oneagent from your kubernetes clusters, such as CPU, memory, disk, network, and container metrics. You can filter, sort, and drill down into the details of each metric. You can also create custom charts and dashboards based on the metrics.
•	Kubernetes logs: This dashboard shows the logs that are collected by oneagent from your kubernetes pods and containers. You can filter, sort, and drill down into the details of each log. You can also search, analyze, and alert on the logs.
•	Kubernetes traces: This dashboard shows the traces that are collected by oneagent from your kubernetes pods and containers. You can filter, sort, and drill down into the details of each trace. You can also see the end-to-end transaction flow and the service map of your kubernetes applications.
For more information on how to use these features, refer to the dynatrace documentation: [URL]/

