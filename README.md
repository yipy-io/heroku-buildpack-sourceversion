# heroku-buildpack-sourceversion

As documented in the [buildpack API](https://devcenter.heroku.com/articles/buildpack-api), Heroku exposes the `SOURCE_VERSION` environment variable during the build process. To make it available during application runtime, this buildpack exports it as an environment variable.


