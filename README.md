# workbench-docker
Docker config for Workbench production deployment. This relies on predefined docker-hub images generated from the main [workbench repo](https://github.com/cjworkbench/cjwowrkbench)

There are different branches for `staging` and `production`, so that `update-staging` is not available on production and vice-versa. This is because `update-staging` tags the image it deploys with `deployed` which `update-production` uses to always deploy exactly the same image.

For more documentation, please see https://github.com/cjworkbench/cjworkbench/wiki/Deployment
