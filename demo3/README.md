# Demo 3

This demo shows how to deploy apps to Kubernetes using [Helm](https://helm.sh). Helm provides several major features that make it an excellent choice for managing production applications in a complex, multi-developer deployment pipeline, such as deploying from CI/CD systems:

- Allows you to bundle, parameterize, and distribute multiple Kubernetes resources all as one "app", called a Chart in Helm lingo
- Allows you to atomically deploy a chart
- Allows you to track each deployment as a release, complete with rolling back and auditing each release

## Demo Instructions

You need to have a working Kubernetes cluster, and your `kubectl` tool configured to access the cluster. After you've done so, run the below command:

```shell
helm upgrade xkcd . --namespace appinnovation --create-namespace --install
```

>This command will both install the application _and_ re-deploy it, should you decide to change the chart or otherwise update the application.
