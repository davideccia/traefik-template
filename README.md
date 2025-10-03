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

- copy the traefik.yaml.example to traefik.yaml
  -  edit it if needed
- go into configuration folder and copy the dynamic.yml.example to dynamic.yaml
  - edit it if needed (for example to edit the traefik password)
- copy the compose.yaml.example to compose.yaml
    - edit it with all you want to deploy
      - remember to use the labels for Traefik

> [!IMPORTANT]
>
> ## ACME
> Create the `acme.json` file in the `data/traefik` dir, and change permissions running `chmod 600 acme.json` on it
>
> ## Network
> Be sure about the `proxy` network exists. If not:
> 
> ```bash
> docker network create proxy
> ```
> 
> ## Labels
> Check all labels into compose.yaml and be sure you have configured it correctly.

## Used for
- [aboutme](https://aboutme.davideccia.click)
- home server
  - [Immich](https://github.com/immich-app/immich)
  - [Nextcloud](https://github.com/nextcloud/)
  - [Jellyfin](https://github.com/jellyfin/jellyfin)
  - [Glance](https://github.com/glanceapp/glance)
