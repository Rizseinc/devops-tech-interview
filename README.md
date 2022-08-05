# devops-tech-interview

Choose one of the [tasks](#tasks) below and complete any number of the optional tasks. There are [multiple questions](#required-questions); add your answers to the `Answer` column. You will have a week from when you receive the email with the link to this repository to complete the required task. These tasks should take roughly two hours to complete. 

Before beginning, fork this repository to your personal GitHub. After completing your task, include the artifacts in the `artifacts` folder under the exercise you chose. When you are ready to submit, create a PR on the parent repository with your changes. For your task, provide instructions on setting up a local environment and deploying the resources. Feel free to ask for clarification or additional information on these tasks.

# Required Questions

| no. | Question | Answer |
| --- | --- | --- |
| 1 | You have three networks hosted in different data centers. The resources on these networks must communicate over a private network. How would you enable communication between the VMs on the networks? |  |
| 2 | Describe what PKI is and how to build a chain of trust |  |
| 3 | A Kubernetes pod fails to start with the error "Image Pull Backoff". What scenarios could cause this error, and how would you resolve them? |  |

# Tasks

## Infrastructure as Code

As a DevOps Engineer, I want a terraform module (or workspace) that creates a public Google Cloud Storage Bucket and hosts the index.html in [exercise/terraform/object-storage-hosting/](exercise/terraform/object-storage-hosting/). Third-party terraform modules are okay to use but creating your own is encouraged.

### Optional

1. All requests should redirect to index.html.
1. Serve the bucket's content as HTTPS from a custom domain.

---

## Container Orchestration

As a DevOps Engineer, I want a HA Kubernetes application deployment of the Dockerfile in [exercise/k8s/orchestration/](exercise/k8s/orchestration/). Expose the deployment using Kubernetes best practices and ingress. 

> assume the nodes are evenly distributed across three availability zones and have the label. `topology.gke.io/zone`

### Optional

1. Ensure the Kubernetes schedules the pods evenly distributed across the available nodes. i.e., one pod per zone.
1. Create a helm chart to make the manifests reusable.

---
