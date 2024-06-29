# heroku-buildpack-sourceversion

As documented in the , Heroku exposes the `SOURCE_VERSION` environment variable during the build process. 

From the [buildpack API docs](https://devcenter.heroku.com/articles/buildpack-api), this is `the "version" of the source code currently being built. For git-push builds, this is the git commit SHA-1 hash.` 

Access to `SOURCE_VERSION` is useful for reporting exactly which version the server is running. To make it available during application runtime, this buildpack exports it as an environment variable.
