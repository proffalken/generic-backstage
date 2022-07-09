# Generic Backstage

This repo contains a generic installation of [Backstage](https://backstage.io) that you can fork
and reuse.

Unlike the stock Backstage, this repo comes with the following plugins pre-installed:

   * [Prometheus](https://roadie.io/backstage/plugins/prometheus)
   * [Github Insights](https://roadie.io/backstage/plugins/github-insights/)
   * [Github Pull Requests](https://roadie.io/backstage/plugins/github-pull-requests)

with more to be added in future.

## Local Development

To start the app locally, run:

```sh
yarn install
yarn dev
```

## Deployment

This repo is designed to be deployed to [Heroku](https://www.heroku.com/) via [Github Actions](https://github.com/features/actions).

All the deployment chain is already setup in the `.github/workflows` directory, all you need to do is set the following secrets in your Github repo settings:

| Secret Name | Description |
|-------------|-------------|
| HEROKU_API_KEY | The API Key you get from your Heroku Account |
| HEROKU_APP_NAME | The name of the application in Heroku.      |

Once the Github Action has been run, you will have a pre-built container ready for you to release to your application infrastructure.
