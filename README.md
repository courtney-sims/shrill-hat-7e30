<!-- dash-content-start -->

Testing hyperdrive

<!-- dash-content-end -->

> [!IMPORTANT]
> When using C3 to create this project, select "no" when it asks if you want to deploy. You need to follow this project's [setup steps](https://github.com/cloudflare/templates/tree/main/d1-template#setup-steps) before deploying.

## Getting Started

Outside of this repo, you can start a new project with this template using [C3](https://developers.cloudflare.com/pages/get-started/c3/) (the `create-cloudflare` CLI):

```
npm create cloudflare@latest -- --template=cloudflare/templates/shrill-hat-7e30
```

A live public deployment of this template is available at [https://shrill-hat-7e30.templates.workers.dev](https://shrill-hat-7e30.templates.workers.dev)

## Setup Steps

1. Install the project dependencies with a package manager of your choice:
   ```bash
   npm install
   ```
2. Create a [Hyperdrive configuration](https://developers.cloudflare.com/hyperdrive/get-started/) with the name "hyperdrive-configuration":
   ```bash
   npx wrangler hyperdrive create hyperdrive-configuration --connection-string="postgres://<DB_USER>:<DB_PASSWORD>@<DB_HOSTNAME_OR_IP_ADDRESS>:5432/<DATABASE_NAME>"
   ```
   ...and update the `hyperdrive` `id` field in `wrangler.json` with the new Hyperdrive ID. You can also specify a connection string for a local PostgreSQL database used for development using the `hyperdrive` `localConnectionString` field.
3. Deploy the project!
   ```bash
   npx wrangler deploy
   ```
