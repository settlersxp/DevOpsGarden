When kubernetes is used to manage containers, the containers are called pods. A pod is a group of one or more containers that are deployed together on the same host. 
Pods are the smallest deployable units of computing that can be created and managed in Kubernetes.

Being an orchestration platform it can also manage the lifetime of the pods, scaling them up or down, restarting them, 
and even moving them to different hosts. Unlike docker-compose, Kubernetes can also manage the networking between the 
pods and the storage that is used by the pods. The storage can be local or in a different cloud provider.

The layer on top of Kubernetes, which handles the hardware scale up is called Terraform.