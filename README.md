# Open Source PaaS/FaaS List

Platform as a Service simplifies and streamlines deployment.

Yes, I can use ssh+vi to manage servers. I did this since 1998, but ssh+vi is not 
a professional way to manager servers.

Yes, I know how to use configuration management (SaltStack or Ansible) to manage servers. But this misses
the streamlining effect, which you get from a PaaS solution.

I know the basics of Kubernetes. But Kubernetes has too many options. That's ok for me, but I am looking for solution
which is simpler for the end user. 

Since Kubernetes has won the container-orchestration race, I am looking for a solution based on Kubernetes.

For completness some non-Kubernetes solutions are listed, too.

Up to now this is just brainstorming. I don't know the conrete goal nor the next steps.

Function-as-a-Service solutions are welcome, too.

Please ping me, if you know an open source solution which is not on the list yet or if you just want chat/talk about this topic. Direct messages are welcome.

# Vague Goal

Make it easy for the end user.

With "end user" being a developer who can create containers, and wants to run them.

## Wishlist

* As end user I just want to run stateless containers. Integrating stateful services like database and storage should be like plug-and-play.
* GitOps
* Accessing kuberenetes via Cluster-API.
* Cluster-API: Adding noes on demand should work out of the box.
* Scale to zero: If there is no traffic, then the application should not consume ressources.
* Cert management (letsencrypt)
* Documentation. I don't want to be the first who tries to get a Django based solution running on it.

## Dokku

Dokku copies Heroku. I guess this is very great if you want to switch from Heroku to a self-hosted solution. But this
is not my use case.

It is mostly written in Shell. I don't trust Shellscripts, but the author is maintaining it with love since several years. Looks stable.

First I thought "herokuish buildscripts" are great, but maybe this mixes two things which don't belong together: Creating a container and running a container.

Multi-Host: No

Container-Orchestration: Kubernetes (but up to now this Sheduler is experimental)


## CapRover

[CapRover](https://github.com/caprover/caprover)

Has a web-GUI.

Written in Typescript.

Nice docs.

Nice feature [Rollback to previous Docker Image](https://caprover.com/docs/deployment-methods.html#one-click-rollback)

The docs advertise DigitalOcean, but CapRover runs on Hetzner or any other VPS.

Multi-Host: Yes 

Container-Orchestration: Docker-Swarm

## Coolify

[Coolify](https://github.com/coollabsio/coolify)

You can add whatever you like for description, it is a caprover alternative / similar to a self hosted heroku/dokku with a gui. (Updates very often)

## LocalCloud

[LocalCloud](https://github.com/localcloud-dev/localcloud-agent)

Multi-cloud PaaS with autoscaling, CI/CD, TLS certificates, VPN, and localhost tunnels.

## Tsuru

[Tsuru](https://tsuru.io/)

Written in go.

Multi-Host: Yes

Container-Orchestration: Docker-Swarm

## porter.run

https://porter.run/

License: Mit + ee directory (unsure if usable without ee)

Container-Orchestration: Kubernetes

# OpenFaaS

Homepage: [https://www.openfaas.com](https://www.openfaas.com)
GitHub: [https://github.com/openfaas](https://github.com/openfaas)

License: MIT

Container-Orchestration: Kubernetes and containerd through [faasd](https://github.com/openfaas/faasd)

"OpenFaaS® makes it simple to deploy both functions and existing code to Kubernetes"

* [View contribution statistics from GitHub](https://kenfdev.o6s.io/github-stats-page)
* [View ADOPTERS file](https://github.com/openfaas/faas/blob/master/ADOPTERS.md)

# Knative

Container-Orchestration: Kubernetes

License: Apache-2.0

# Flinkwerk


https://flinkwerk.com/

Container-Orchestration: Kubernetes

License: unsure. In Beta, not released yet

# Kubernetes

Most people don't see Kubernetes as a PaaS, since you don't have a web GUI for
configuring the system.

At least at the moment every PaaS will be some kind of vendor-lockin, even if you
choose an open source PaaS.

Maybe it is best to embrace the complexity which Kubernetes brings. Compared to running
several VM based solutions, Kubernetes is not much harder.

Kubernetes has the benefit that the basics are streamlined. 

Containers, Pods, Deployments, Services, Ingresses. These things are well defined.

Compare this managing several virtual machines. There are far too many ways to run
several VMs. From this perspective Kubernetes is not that complicated.

# OpenFunction

https://openfunction.dev/


# WOL

[Thomas Working-out-Loud](//github.com/guettli/wol)

