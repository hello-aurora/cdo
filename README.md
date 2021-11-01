# heroku-buildpack-cdo

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) working with [`heroku-20`](https://devcenter.heroku.com/articles/stack) for vendoring the [cdo](https://code.mpimet.mpg.de/projects/cdo) library into your project.

### Install

In your project root:

`heroku buildpacks:add https://github.com/hello-aurora/cdo --index 1 --app HEROKU_APP_NAME`

### Clear cache

Since the installation is cached you might want to clean it out due to config changes.

1. `heroku plugins:install heroku-repo`
2. `heroku repo:purge_cache --app HEROKU_APP_NAME`
