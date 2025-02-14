<p align="center">
    <picture>
      <img style="border-radius:10%; background-color: white;" width="30%" title="Logo" alt="Logo" src="https://raw.githubusercontent.com/docker-library/docs/a6cc2c5f4bc6658168f2a0abbb0307acaefff80e/traefik/logo.png">
    </picture>
</p>

# Traefik reverse proxy template
An easy way use the Traefik reverse proxy with docker-compose.


## Prerequisites
- Docker

## Steps

- copy the traefik.yml.example to traefik.yml
  -  edit it if needed
- go into configuration folder and copy the dynamic.yml.example to dynamic.yml
  - edit it if needed (for example to edit the traefik password)
- copy the docker-compose.yml.example to docker-compose.yml
    - edit it with all you want to deploy

> [!IMPORTANT]
>
> ## ACME
> Create the `acme.json` file in the `traefik` dir, and change permissions running `chmod 600 acme.json` on it
>
> ## Network
> Be sure about the `proxy` network exists. If not:
> 
> ```bash
> docker network create proxy
> ```
> 
> ## Labels
> Check all labels into docker-compose.yml and be sure you have configured it correctly.
> 
> **DON'T MISS OUT THIS LABEL** 
> 
> The `traefik.http.services.portainer.loadbalancer.server.port=xxxx` label is where Traefik will internally redirect. 
> 
