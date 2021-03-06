# Docker-Cheatsheet

## Articles
* Docker Compose
  * [Running Multiple Instances of a Service](https://pspdfkit.com/blog/2018/how-to-use-docker-compose-to-run-multiple-instances-of-a-service-in-development/)
* Docker Machine
  * [Adding Existing Digital Ocean Droplets to Docker-Machine](https://medium.com/rayn-studios/adding-existing-digital-ocean-droplet-to-docker-machine-93dfb28e1d96)
  * [Mounting docker-machine Volumes Into Containers](https://docs.docker.com/machine/reference/mount/)
* Docker Cleanup
  * [Remove Images/Containers/Volumes](https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes)
* Miscellaneous
  * [Dockerizing Angular CLI App](https://mherman.org/blog/dockerizing-an-angular-app/)

## Helpful Commands

Create a DigitalOcean Droplet with `docker-machine`:
```bash
docker-machine create \
  --driver digitalocean \ 
  --digitalocean-access-token <API ACCESS TOKEN> \
  <DROPLET NAME>
```

Connect `docker-machine` to an existing DigitalOcean Droplet:
```bash
docker-machine create \
  --driver generic \
  --generic-ip-address <DROPLET IPv4> \
  --generic-ssh-user root \
  --generic-ssh-key="~/.ssh/id_rsa" \
  <DROPLET NAME>
```
*Note: On Windows you may have to provide the full path to your ssh key*

