---
id: try-tooljet
title: Try ToolJet
---

# Try ToolJet
## On local with Docker

You can run the command below to have ToolJet up and running right away.

```bash
docker run \
  --name tooljet \
  --restart unless-stopped \
  -p 80:80 \
  -v tooljet_data:/var/lib/postgresql/13/main \
  tooljet/try:latest
```

#### Setup information

- Runs the ToolJet server on the port 80 on your machine.
- Container has postgres already configured within. All the data will be available in the docker volume `tooljet_data`.
- Default user credentials to login (email: `dev@tooljet.io`, password: `password`).
- You can make use of `--env` or `--env-file` flag to test against various env configurables mentioned [here](https://docs.tooljet.com/docs/setup/env-vars).
- Use `docker stop tooljet` to stop the container and `docker start tooljet` to start the container thereafter.

## On Play with docker

You can deploy ToolJet on PWD for free with the one-click-deployment button below.

  <a href="https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/ToolJet/ToolJet/main/deploy/docker/play-with-docker.yml">
    <img src="https://raw.githubusercontent.com/play-with-docker/stacks/master/assets/images/button.png" alt="Try in PWD" height="32"/>
  </a>

#### Setup information

- Default user credentials to login (email: `dev@tooljet.io`, password: `password`).
- Open port 80 after the docker containers are up and running
- Visit the url shared on the dashboard to try out tooljet
