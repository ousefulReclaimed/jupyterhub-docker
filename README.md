# JupyterHub deployment for use On Reclaim.Cloud

This is a [JupyterHub](https://jupyter.org/hub) deployment based on
Docker originally inspired by [`defeo/jupyterhub-docker`](https://github.com/defeo/jupyterhub-docker) (described [here](https://opendreamkit.org/2018/10/17/jupyterhub-docker/)), partially funded by the EU H2020 project [OpenDreamKit](https://opendreamkit.org/), and as used at the [Université de
Versailles](https://jupyter.ens.uvsq.fr/).

## Features

- Containerized single user Jupyter servers, using
  [DockerSpawner](https://github.com/jupyterhub/dockerspawner);
- first use authenticator;
- User data persistence;

The HTTPs reverse-proxy as used in the original has been removed with the intention that https and load reverse-proxy support are provided by the Jelastic platfrom on the host.

### Adapt to your needs

Then, if you like, clone this repository and apply (at least) the
following changes:


### Run!

In Reclaim.Cloud:

- create a new environment;
- select the docker engine / docker-compose setup and create;
- open web ssh terminal;
- run:

```
git clone --branch reclaim https://github.com/ouseful-testing/jupyterhub-docker/
cd jupyterhub-docker
docker-compose up -d
```

Read the [Docker Compose manual](https://docs.docker.com/compose/) to
learn how to manage your application.
