# CDO

Buildpack for vendoring the [cdo](https://code.mpimet.mpg.de/projects/cdo) library into your project. Can be used with [Heroku](https://www.heroku.com) or [Dokku](https://dokku.com/).

After the installation process, you will be able to access the following libraries:

- [zLib](https://www.zlib.net/)
- [HDF5](https://portal.hdfgroup.org/display/HDF5/HDF5)
- [NetCDF](https://www.unidata.ucar.edu/software/netcdf/)
- [ecCodes](https://confluence.ecmwf.int/display/ECC)
- [CDO](https://code.mpimet.mpg.de/projects/cdo)

> CDO requires a lot of memory. You might need > 1GO of RAM.

## Installation

Heroku:

```bash
heroku buildpacks:add https://github.com/hello-aurora/cdo --index 1 --app <APP_NAME>
```

Dokku:

```bash
dokku buildpacks:add --index 1 <APP_NAME> https://github.com/hello-aurora/cdo
```

## Clear cache

Since the installation is cached you might want to clean it out due to config changes.

Heroku:

```bash
heroku plugins:install heroku-repo
heroku repo:purge_cache --app <APP_NAME>
```

Dokku:

```bash
dokku repo:purge-cache <APP_NAME>
```
