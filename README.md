# cjworkbench-docker
Docker config for CJWorkbench production deployment. This relies on predefined docker-hub images generated from the main [cjworkbench repo](https://github.com/jstray/cjworkbench)

# First time start

Create containers and volumes: `docker-compose up -d`

Then create an admin user like this:

`docker exec -it cjw-web python manage.py shell -c "from django.contrib.auth.models import User; User.objects.create_superuser('admin', 'admin@cjworkbench.org', 'admin')`

# Starting and stopping

Use `docker-compose up -d` and `docker-compose down`

# To update

```
docker-compose down
docker-compose pull
docker-compose up -d
```

# To run commands inside server context
`docker exec -it cjw-web bash`

