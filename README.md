# App Innovation Webinar - January 12, 2021

Demo code for my talk at the Azure App Innovation Webinar. This repository has 3 demos in it:

- [demo 1](./demo1) - basic Kubernetes resources required to deploy an HTTP server and expose it to the internet on [Azure Kubernetes Service](https://azure.microsoft.com/en-us/services/kubernetes-service/)
  - Note: do not use this demo for a production web app. It does not include several features necessary for a secure and robust application on the internet
- [demo 2](./demo2) - an overview of the [KEDA](https://keda.sh) project and the alpha-status [KEDA HTTP](https://github.com/kedacore/http-add-on) project
- [demo 3](./demo3) - an overview of [Helm](https://helm.sh) and how to deploy, audit, and maintain your Kubernetes-based app over time
