* [Msdn static app pipeline task](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/azure-static-web-app-v0?view=azure-pipelines)

Azure web static task
```js
# Deploy Azure Static Web App v0
# Build and deploy an Azure Static Web App.
- task: AzureStaticWebApp@0
	inputs:
		#workingDirectory: '$(System.DefaultWorkingDirectory)' # string. Alias: cwd | rootDirectory. Working directory. Default: $(System.DefaultWorkingDirectory).
		#app_location: # string. App location.
		#app_build_command: # string. App build command.
		#output_location: # string. Output location.
		#api_location: # string. Api location.
		#api_build_command: # string. Api build command.
		#routes_location: # string. Routes location.
		#config_file_location: # string. Config file location.
		#skip_app_build: # boolean. Skip app build.
		#skip_api_build: # boolean. Skip api build.
		#is_static_export: # boolean. Set static export.
		#verbose: # boolean. Verbose.
		#build_timeout_in_minutes: # string. Build timeout in minutes.
		#azure_static_web_apps_api_token: # string. Azure Static Web Apps api token.
		#deployment_environment: # string. Deployment Environment.
		#production_branch: # string. Production Branch.
```