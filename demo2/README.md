# Demo 2

In this demo, we'll be deploying an HTTP server to Kubernetes that automatically scales based on incoming traffic. This functionality is made possible by [KEDA](https://github.com/kedacore/keda) and [KEDA-HTTP](https://github.com/kedacore/http-add-on).

The former, KEDA, is a battle-tested generic framework for enabling Kubernetes workloads that automatically scale based on a variety of external systems like Azure Event Hubs, Azure Log Analytics, several other Azure service and a variety of other services from other clouds and open source systems. It doesn't, however, support HTTP, which is where the latter KEDA-HTTP system steps in.

KEDA-HTTP is an extension to KEDA that:

- Intelligently routes HTTP traffic from a source such as the  instructs KEDA to scale a backend  `Deployment`
- Reports to KEDA whether, and how it should scale the aforementioned `Deployment`

>The `KEDA-HTTP` software we'll be using in this demo is alpha status. This demo will be based on a [prototype implementation](https://github.com/osscda/kedahttp). The first beta release will be available later this month (January 2021) or early next (February 2021) in [this repository](https://github.com/kedacore/http-add-on).

## Demo Instructions

This demo is based on several repositories and custom-compiled code, so is difficult to replicate right now. It's intended to show the power of KEDA and the new KEDA-HTTP project.

Please watch the [KEDA-HTTP](https://github.com/kedacore/http-add-on) repository for developments in the next few weeks. We'll be releasing a beta soon, at which point it will be possible to take full advantage of this technology.
