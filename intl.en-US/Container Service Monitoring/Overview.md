# Overview

Cloud Monitor automatically collects metrics of all the Container Service for Kubernetes \(ACK\) clusters that belong to your Alibaba Cloud account. This allows you to centrally manage your ACK clusters that are deployed in multiple regions.

## Terms

For information about terms such as cluster, node, namespace, workload, and pod of ACK, see [Terms](/intl.en-US/Product Introduction/Terms.md).

For information about ACK, see [What is Container Service for Kubernetes?](/intl.en-US/Product Introduction/What is Container Service for Kubernetes?.md).

## Metrics

For information about the metrics of clusters, nodes, namespaces, applications, and pods of ACK, see [ACK \(new version\)]().

## Features

The following table describes the features that are supported by Container Service Monitoring.

|Feature|Description|
|-------|-----------|
|[View monitoring data]()|Provides an overview of ACK clusters and monitoring data of nodes, namespaces, and workloads of ACK clusters. This feature allows you to track the running status of ACK clusters.|
|[Manage alert rules]()|Allows you to configure alert rules for ACK clusters, nodes, and pods. When an alert is triggered, Cloud Monitor sends an alert notification. This way, you are immediately notified of exceptions and can handle the exceptions at the earliest opportunity.|

## Limits

Before Cloud Monitor can monitor ACK clusters, you must update the metrics-server component of the clusters to V0.3.8 or later. For more information, see [Install the metrics-server component](/intl.en-US/User Guide for Kubernetes Clusters/Cluster management/Upgrade cluster/Install the metrics-server component.md).

