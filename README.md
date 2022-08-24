# Huawei Cloud - CCE Service - GitHub Actions

## Requirements

You need to have the following services already created in your Huawei Cloud account:

- Huawei Cloud CCE Service
- Huawei Cloud ELB Service
- Huawei Cloud SWR Service

You need to add the following secrets under github repository -->settings-->Actions in advance.

1. HC_ACCESS_KEY_ID : Access Key of your Huawei Cloud account
2. HC_ACCESS_KEY_SECRET : Secret Key of your Huawei Cloud account
3. HC_CCE_PROJECT_ID : Project ID of your Huawei Cloud account
4. HC_CCE_CLUSTER_ID : Cluster ID of your CCE Kubernetes cluster
5. HC_CCE_KUBECONFIG : Kubeconfig file of your CCE Kubernetes cluster
6. SWR_ENDPOINT : Endpoint of SWR service
7. SWR_ORGANIZATION_NAME : Organization Name in the SWR service

## Description

This is a demo code of how to build a GitHub Actions pipeline to automate CI/CD deployments in Kubernetes cluster on Huawei Cloud.

The Git Hub Actions workflow consist on the following steps:

- Login to SWR Service.
- Check out the code of the Git Hub repo.
- Build the Docker image.
- Push the Docker image to SWR Service.
- Login to CCE Service (Kubernetes cluster).
- Deploy to CCE a demo app using a deployment and service (ELB) kinds.

For this demo we are using a .NET Core docker image.
For more information, check out https://docs.microsoft.com/en-us/dotnet/core/docker/build-container?tabs=windows 
