# Open Source PaaS List

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

## Tsuru

[Tsuru](https://tsuru.io/)

Written in go.

Multi-Host: Yes

Container-Orchestration: Docker-Swarm

## porter.run

https://porter.run/

License: Mit + ee directory (unsure if usable without ee)

Container-Orchestration: Kubernetes

# Open FaaS

https://www.openfaas.com/

License: MIT

Container-Orchestration: Kubernetes

Note: If you look at this statistic, you might think that OpenFaaS is a one-man-show [Github contributors](https://github.com/openfaas/faas/graphs/contributors). But this is not true. This repo that is one small part of a very large project with 40+ repositories. A better overview: https://kenfdev.o6s.io/github-stats-page#/

# Knative

Container-Orchestration: Kubernetes

License: Apache-2.0

# Flinkwerk


https://flinkwerk.com/

Container-Orchestration: Kubernetes

License: unsure. In Beta, not released yet



# WOL

[Thomas Working-out-Loud](//github.com/guettli/wol)

