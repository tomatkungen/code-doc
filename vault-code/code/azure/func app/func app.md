* [v4 func app](https://techcommunity.microsoft.com/t5/apps-on-azure-blog/azure-functions-version-4-of-the-node-js-programming-model-is-in/ba-p/3773541)


```shell
# install func app core tool cli
brew tap azure/functions
brew install azure-functions-core-tools@4 

# if upgrading on a machine that has 2.x or 3.x installed: 
brew link --overwrite azure-functions-core-tools@4
```

```shell
# Deploy function app in cmd
func azure functionapp publish <FunctionAppName>

# Deploy function app in cms with local.settings.json, ConnectionStrings is never # publish
func azure functionapp publish <FunctionAppName> --publish-local-settings
```

```shell
#Receiving log streams from function app
func azure functionapp logstream <FunctionAppName>
```

```shell
# when start function apps the url is in the browser
http://localhost:<port>/api/<function_name>

# Call Get request with curl in terminal
curl --get http://localhost:7071/api/MyHttpTrigger?name=Azure%20Rocks

# Call Post request with curl in terminal
curl --request POST http://localhost:7071/api/MyHttpTrigger --data "{'name':'Azure Rocks'}"
# or
curl --request POST -H "Content-Type:application/json" --data "{'input':'sample queue data'}" http://localhost:7071/admin/functions/QueueTrigger

# Call Post request with curl in bash script
curl --request POST http://localhost:7071/api/MyHttpTrigger --data '{"name":"Azure Rocks"}'
# or
curl --request POST -H "Content-Type:application/json" --data '{"input":"sample queue data"}' http://localhost:7071/admin/functions/QueueTrigger

# when start functions apps you can get all functions calling
http://localhost:<port>/admin/functions/
http://localhost:<port>/admin/functions/<function_name>

```

* [Local settings json properties msdn](https://learn.microsoft.com/en-us/azure/azure-functions/functions-develop-local#local-settings-file)
```json
// local.settings.json structure
{
  "IsEncrypted": false,
  "Values": {
    "FUNCTIONS_WORKER_RUNTIME": "<language worker>",
    "AzureWebJobsStorage": "<connection-string>",
    "MyBindingConnection": "<binding-connection-string>",
    "AzureWebJobs.HttpExample.Disabled": "true"
  },
  "Host": {
    "LocalHttpPort": 7071,
    "CORS": "*",
    "CORSCredentials": false
  },
  "ConnectionStrings": {
    "SQLConnectionString": "<sqlclient-connection-string>"
  }
}
```