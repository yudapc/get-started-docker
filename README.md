# Get started Docker Compose

source: https://docs.docker.com/compose/gettingstarted/

### Create Dockerfile

- Added folder project
- Install packages
- Start App

---

### Create docker-compose.yml

- Setup Services (web, redix, nginx, etc)

---

### Run

This command for run docker:

`docker-compose up`

Or running in background:

`docker-compose up -d`

---

### List Docker Containers

`docker-compose ps`

```
           Name                         Command               State           Ports
--------------------------------------------------------------------------------------------
docker-composetest_redis_1   docker-entrypoint.sh redis ...   Up      6379/tcp
docker-composetest_web_1     python app.py                    Up      0.0.0.0:5000->5000/tcp
```

---

### SSH to docker container

`docker exec -it <docker-container-name> sh`

---

### Stop

If you started Compose with docker-compose up -d, stop your services once you’ve finished with them:

`docker-compose stop`

---

### Down

You can bring everything down, removing the containers entirely, with the down command. Pass --volumes to also remove the data volume used by the Redis container:

`docker-compose down --volumes`
