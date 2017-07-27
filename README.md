# cjworkbench-docker
Docker config for CJWorkbench production deployment. This relies on predefined docker-hub images generated from the main [cjworkbench repo](https://github.com/jstray/cjworkbench)

# First time start

Set production settings environment variables for your shell: `source ~/.env`
Create containers and volumes: `docker-compose up -d`

Then create an admin user like this:

`docker exec -it cjw-web python manage.py shell -c "from django.contrib.auth.models import User; User.objects.create_superuser('admin', 'admin@cjworkbench.org', 'admin')`

# Starting and stopping

Make sure you've done `source ~/.env`
Use `docker-compose up -d` and `docker-compose down`

# To update

Make sure you've done `source ~/.env`

```
docker-compose down
docker-compose pull
docker-compose up -d
```

# To run commands inside server context
`docker exec -it cjw-web bash`

