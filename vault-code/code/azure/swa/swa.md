* Static Web App (SWA)
* [homepage swa](https://azure.github.io/static-web-apps-cli/docs/use/install) 
* swa commands
	*   [`login`](https://azure.github.io/static-web-apps-cli/docs/cli/swa-login): login into Azure
	-   [`init`](https://azure.github.io/static-web-apps-cli/docs/cli/swa-init): initialize a new static web app project
	-   [`start`](https://azure.github.io/static-web-apps-cli/docs/cli/swa-start): start the emulator from a directory or bind to a dev server
	-   [`deploy`](https://azure.github.io/static-web-apps-cli/docs/cli/swa-deploy): deploy the current project to Azure Static Web Apps
	-   [`build`](https://azure.github.io/static-web-apps-cli/docs/cli/swa-build): build your project

```shell
# install in directory
yarn add -D @azure/static-web-apps-cli
```

```shell
# Check swa version
yarn swa --version
```

```shell
# start proxy for dev server
yarn swa start <dev-server-url>

# start server and run code in dist
yarn swa start <dist path>

# Ex:
yarn swa start ./client/dist
```

```shell
# Start proxy and dev server
yarn swa start <dev-server-url> --run <dev-server-launch-cmd>

# Ex:
yarn swa start http://localhost:3000 --run "yarn --cwd ./client/ dev"
```

```shell
# Start proxy web client host -> to -> func app host api
yarn swa start <dev-server-url> --api-devserver-url <api-dev-server-url>

# Ex:
yarn swa start http://localhost:5173/ --api-devserver-url http://localhost:7071
```

```shell
# List all swa-cli.config.json options
yarn swa --print-config
```