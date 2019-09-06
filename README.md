# Nexus OSS in AWS EKS Cluster through Helm Chart

>  Nexus OSS is a free open source private repository manager. It supports a wide range of package formats and it's used by hundreds of tech companies.

This chart deploys Sonatype Nexus OSS repository manager in a Kubernetes Cluster. This setup is best configured in AWS EKS (Amazon Elastic Kubernetes Service) since:

- AWS S3 (Amazon Simple Storage Service) is used for backups
- AWS ECR (Amazon Elastic Container Registry) is used for managing container images


### Prerequisites

- AWS ECR (or any other Docker registry manager to manage container images)
- AWS EKS Cluster with Autoscaling, External DNS and required IAM roles enabled and nodes that fulfill Nexus requirements. A very good place to start : 
  https://github.com/alamscode/generalized/tree/rogue_one/terraform/terraform-eks


### How to:

Clone the reository. 
Edit the "Helm/Nexus/values.yaml" file according to your infrastructure and needs. Then install the helm chart into the cluster.