# Overview

MayaOnline.io is a first solution of its type  and is free for basic usage. It leverages the cross-cloud capabilities of Kubernetes and containers themselves and extends them to the data-plane with the help of the fully containerized OpenEBS. This solution is called a “Cross-cloud data-plane”.

Self management of storage for **DevOps**, with the help of software.

**Free **visibility into **Kubernetes **with **ChatOps ** and cross cloud control.

# MayaOnline Workflow

![](/assets/MayaOnline %287%29.png)

# Why MayaOnline

MayaOnline.io - Is the first solution of its type. And it is free for basic usage. It leverages the cross-cloud capabilities of Kubernetes and containers themselves and extends them to the data-plane with the help of the fully containerized OpenEBS. We call the solution a “Cross-cloud data-plane”.

## **Analytics**

* MayaOnline shows how workloads are performing and consuming data across clouds; for example, which storage policies result in higher performance for your workloads, irrespective of the underlying cloud vendor or data center?
* MayaOnline analytics are based on the CNCF project Prometheus. Prometheus is noted for its scalability and usefulness in distributed environments. Much more about Prometheus here: https://prometheus.io

  At the centre of our architecture, MayaOnline runs a Prometheus system for each user and interacts with the Prometheus node exporters of each cluster in user’s cloud deployments or in user’s on-premise instances. These time-series data entries are centrally stored and curated on user’s prometheus instance on MayaOnline.

  Intuitive graphs are delivered using Grafana.

## Monitoring

## **ChatOps and other controls**

* In addition to the graphical interface enabling analytics and the creation and management of automations, ChatOps is used to communicate with users. MayaOnline can post status to Slack channels and users can initiate actions from these channels that MayaOnline will execute. ChatOps also will enable developers and administrators to respond to data related alerts and also query the data plane from slack itself.

## **API driven**

* While ChatOps is useful to keep the users in the loop, many decisions in large environments are made as a part of a pipeline or other automation. MayaOnline can be queried for relevant information or can proactively post information via its Rest APIs.

## **cMotion**

* MayaOnline will be able to balance workloads across clouds proactively. This balancing is implemented in a Kubernetes friendly way - where OpenEBS instances are reconfigured along with the storage policies that are used by Kubernetes to control them. At KubeCon 2017 in Austin, we are demonstrating cross-cloud balancing where workloads \(both stateless and stateful\) from one cloud are automatically replicated to other cloud vendor and made available in that cloud. This capability will be expanded significantly in 2018.

MayaOnline includes initial cMotion capabilities. These rely upon the power of individual OpenEBS containers which - if they are using the new cStore storage engine - have the ability to deliver copy on write based snapshots. These snapshots - and the approach to writing data to disk itself - are inherently safer and more efficient than many other approaches to replication. When used for replication, this approach means that only changes to the underlying data are sent across the network to the far end. The entire experience of moving the OpenEBS data containers across user’s Kubernetes clusters is seamlessly handled by MayaOnline.


