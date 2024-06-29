# heroku-buildpack-sourceversion

Heroku exposes the `SOURCE_VERSION` environment variable, but only during the build process. 

From the [buildpack API docs](https://devcenter.heroku.com/articles/buildpack-api), this is `the "version" of the source code currently being built. For git-push builds, this is the git commit SHA-1 hash.` 

Access to `SOURCE_VERSION` is useful for reporting exactly which code the server is running. To make it available during runtime, this buildpack writes it to the `.source_version` file in the application build directory.

Add this to your application with: `heroku buildpacks:add https://github.com/yipy-io/heroku-buildpack-sourceversion.git`