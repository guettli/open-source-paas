# Open Source PaaS List

Platform as a Service simplifies and streamlines deployment.

Yes, I can use ssh+vi to manage servers. I did this since 1998, but ssh+vi is not 
a professional way to manager servers.

Yes, I know how to use configuration management (SaltStack or Ansible) to manage servers. But this misses
the streamlining effect, which you get from a PaaS solution.

PaaS are usualy using some kind of containers to execute the applications.

## Required Features

* As a software developer I want to deploy a several Django based app on one VPS.
* I don't want to run a big infrastructure, I just have one VPS. Kubernetes based solutions don't make sense for me at the moment.
* I want http. Letsencryptit support is needed.
* Documentation. The PaaS should be documented. I don't want to be the first who tries to get a Django based solution running on it.

## Dokku

Dokku copies Heroku. I guess this is very great if you want to switch from Heroku to a self-hosted solution. But this
is not my use case.

It is mostly written in Shell. I don't trust Shellscripts, but the author is maintaining it with love since several years. Looks stable.

Dokku has three ways to operate: herokuish buildscripts, Dockerfiles, Docker-Images.

First I though "herokuish buildscripts" are great, but maybe this mixes two things which don't belong together: Creating a container and running a container.

# Flynn

This was cool some years ago. Now there are 430 open issues, and the development has stalled.

## CloudFoundry

Looks too heavy and too enterprise-like. The tutorial talks about billions of market value, but not how to install it on my VPS.

## CapRover

[CapRover](https://github.com/caprover/caprover)

Has a web-GUI.

Written in Typescript.

Nice docs.

Nice feature [Rollback to previous Docker Image](https://caprover.com/docs/deployment-methods.html#one-click-rollback)

The docs advertise DigitalOcean, but CapRover runs on Hetzner or any other VPS.

## Star-History

![paas-star-history](paas-star-history.png)

Source: [star-history](https://star-history.t9t.io/#caprover/caprover&flynn/flynn&tsuru/tsuru&dokku/dokku)

