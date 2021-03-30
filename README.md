# heroku-buildpack-nodejs-monorepo
Heroku buildpack supporting deployment of Node.js applications within a monorepo

This is based on the example of [Heroku Multi Procfile buildpack](https://github.com/heroku/heroku-buildpack-multi-procfile)

The buildpack expects to find an environment variable, `APP_BASE`, which points to the
relative path of the application directory to publish from within the monorepo.

It also expects to find the `Procfile`, `package.json`, and `package-lock.json`
files within the `APP_BASE` directory.

The `Procfile` should look like:
```
web: cd app-directory && node path/to/app-start.js
```
