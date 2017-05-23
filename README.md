# cjworkbench-docker
Docker config for CJWorkbench production deployment. This relies on predefined docker-hub images generated from the main [cjworkbench repo](https://github.com/jstray/cjworkbench)

# To start
The first time: `docker-compose up`
Thereafter: `docker-compose start`

# To update

```
docker-compose stop
docker-compose pull
docker-compose start
```

WARNING! Do not ever do `docker-compose down` or you will lose the entire database!

# To run commands inside server context
`docker exec -it cjw-web bash`

