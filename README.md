# heroku-buildpack-cdo

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) working with [`heroku-20`](https://devcenter.heroku.com/articles/stack) for vendoring the [cdo](https://code.mpimet.mpg.de/projects/cdo) library into your project.

## Install

In your project root:

`heroku buildpacks:add https://github.com/hello-aurora/cdo --index 1 --app HEROKU_APP_NAME`

## Usage

This buildpack install CDO and its required dependencies.

After the installation process, you will be able to access the following libraries:

- [zLib](https://www.zlib.net/)
- [HDF5](https://portal.hdfgroup.org/display/HDF5/HDF5)
- [NetCDF](https://www.unidata.ucar.edu/software/netcdf/)
- [ecCodes](https://confluence.ecmwf.int/display/ECC)
- [CDO](https://code.mpimet.mpg.de/projects/cdo)

> CDO requires a lot of memory. You might at least need a dyno with > 1GO of RAM.

## Clear cache

Since the installation is cached you might want to clean it out due to config changes.

1. `heroku plugins:install heroku-repo`
2. `heroku repo:purge_cache --app HEROKU_APP_NAME`
