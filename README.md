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

# Goal

Make it easy for the end user.

With "end user" being a developer who can create containers, and wants to run them.

## Required Features

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

Dokku has three ways to operate: herokuish buildscripts, Dockerfiles, Docker-Images.

First I thought "herokuish buildscripts" are great, but maybe this mixes two things which don't belong together: Creating a container and running a container.

Multi-Host: No

With Dokku you can "link" an App to a database. This automatically creates a matching DATABASE_URL. 
See [Linking backing services to applications](http://dokku.viewdocs.io/dokku/deployment/application-deployment/#linking-backing-services-to-applications)
That's cool.


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


# WOL

[Thomas Working-out-Loud](//github.com/guettli/wol)

