<img style="background-color: white" width="30%" title="Logo" alt="Logo" src="https://raw.githubusercontent.com/docker-library/docs/a6cc2c5f4bc6658168f2a0abbb0307acaefff80e/traefik/logo.png">

# For an easy Docker deploy with reverse proxy

## Steps

- copy the acme.json.example to acme.json
    - run `sudo chmod 600 acme.json` on it
- copy the traefik.yml.example to traefik.yml
  -  edit it if needed
- go into configuration folder and copy the dynamic.yml.example to dynamic.yml
  - edit it if needed (for example to edit the traefik password)
- copy the docker-compose.yml.example to docker-compose.yml
    - edit it with all you want to deploy

> [!IMPORTANT]
>
> Check all labels into docker-compose.yml and be sure you have configured it correctly.
> 
> The `traefik.http.services.portainer.loadbalancer.server.port=xxxx` label is where Traefik will redirect. 
> 
> **DON'T MISS OUT THIS LABEL** 