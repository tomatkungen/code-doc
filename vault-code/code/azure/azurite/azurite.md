* Azurite is emulator local for Azure storage
	* Blob, Queue Storage, Table Storage
* Exist in vscode as extension, Build in Visual studio 2022, Docker, github, npm

```shell
# Install npm package in cmd
npm install -g azurite

# Install yarn package in cmd
npm install -D azurite
```

```shell
# Execute azurite in cmd, the --location is current working directory
azurite --silent --location c:\azurite --debug c:\azurite\debug.log

# help in cmd
azurite -h

# Azurite server listen on ip type in cmd
azurite --blobHost 127.0.0.1
azurite --blobPort 8888 # Customize Blob service listening port
azurite --blobPort 0 # Auto select listening port

# Azurite server listen on remote type in cmd
azurite --blobHost 0.0.0.0
```

