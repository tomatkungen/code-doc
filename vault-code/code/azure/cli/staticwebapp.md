* [msdn cli AZ staticwebapp](https://learn.microsoft.com/en-us/cli/azure/staticwebapp?view=azure-cli-latest)
* Get Deployment token
	* [Azure portal](https://portal.azure.com/) -> Home -> Static Web App -> your instance -> overview -> Manage Deployment token

```zsh
# Login to az
az login

# List all static app resource in subscription or in resource group
az staticwebapp list

# Get deployment token application-name = rs-myagent-static-web
az staticwebapp secrets list --name <application-name> --query "properties.apiKey"

```

