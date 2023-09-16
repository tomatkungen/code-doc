* [win cosmos emulator local](https://aka.ms/cosmosdb-emulator)
* [mac cosmos emu local](https://learn.microsoft.com/en-us/azure/cosmos-db/docker-emulator-linux?tabs=sql-api%2Cssl-netstd21)
* [azure cosmos sdk](https://learn.microsoft.com/en-us/javascript/api/overview/azure/cosmos-readme?view=azure-node-latest)
* [apllo graphql datasource](https://github.com/andrejpk/apollo-datasource-cosmosdb)

```shell
# Install cosmos npm package
npm install @azure/cosmos
```

```shell
# Get Cosmos endpoint type in cmd
az cosmosdb show --resource-group <your-resource-group> --name <your-account-name> --query documentEndpoint --output tsv

# Get Cosmos Masterkey type in cmd
az cosmosdb keys list --resource-group <your-resource-group> --name <your-account-name> --query primaryMasterKey --output tsv
```