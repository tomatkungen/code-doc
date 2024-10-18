[install Mac](https://docs.couchdb.org/en/stable/install/mac.html)'

```shell
# browser paste to open fauxton client
http://127.0.0.1:5984/_utils/

```
```shell
# Check DB is running
curl http://127.0.0.1:5984/

# Response
{
  "couchdb": "Welcome",
  "version": "3.0.0",
  "git_sha": "83bdcf693",
  "uuid": "56f16e7c93ff4a2dc20eb6acc7000b71",
  "features": [
    "access-ready",
    "partitioned",
    "pluggable-storage-engines",
    "reshard",
    "scheduler"
  ],
  "vendor": {
    "name": "The Apache Software Foundation"
  }
}
```

```shell
# curl http://<user>:<password>@127.0.0.1:5984
curl http://admin:password@127.0.0.1:5984

# Response
{
  "couchdb": "Welcome",
  "version": "3.0.0",
  "git_sha": "83bdcf693",
  "uuid": "56f16e7c93ff4a2dc20eb6acc7000b71",
  "features": [
    "access-ready",
    "partitioned",
    "pluggable-storage-engines",
    "reshard",
    "scheduler"
  ],
  "vendor": {
    "name": "The Apache Software Foundation"
  }
}
```

```shell
# Create user admin anna with pass secret
> HOST="http://admin:password@127.0.0.1:5984"
> NODENAME="_local"
> curl -X PUT $HOST/_node/$NODENAME/_config/admins/anna -d '"secret"'
""
```

```shell
# Create document
> HOST="http://anna:secret@127.0.0.1:5984"
> curl -X PUT $HOST/somedatabase

#Response
{"ok":true}
```

```shell
# Create a new user
curl -X PUT http://localhost:5984/_users/org.couchdb.user:jan \
     -H "Accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{"name": "tomatkungen", "password": "tomatkunen", "roles": [], "type": "user"}'
# Response 
{"ok":true,"id":"org.couchdb.user:jan","rev":"1-e0ebfb84005b920488fc7a8cc5470cc0"}
```

```shell
# Get all databases
curl -X GET http://admin:password@127.0.0.1:5984/_all_dbs

# Response
["_replicator","_users"]

# Create database
curl -X PUT http://admin:password@127.0.0.1:5984/baseball

# REsponse
{"ok":true}

```

```shell
# Get UUID from database
curl -X GET http://127.0.0.1:5984/_uuids

# Response
{"uuids":["6e1295ed6c29495e54cc05947f18c8af"]}
```

```javascript
- Creating a database ([`PUT /database`](https://docs.couchdb.org/en/stable/api/database/common.html#put--db "PUT /{db}"))
    
- Deleting a database ([`DELETE /database`](https://docs.couchdb.org/en/stable/api/database/common.html#put--db "PUT /{db}"))
    
- Setup a database security ([`PUT /database/_security`](https://docs.couchdb.org/en/stable/api/database/security.html#put--db-_security "PUT /{db}/_security"))
    
- Creating a design document ([`PUT /database/_design/app`](https://docs.couchdb.org/en/stable/api/ddoc/common.html#put--db-_design-ddoc "PUT /{db}/_design/{ddoc}"))
    
- Updating a design document ([`PUT /database/_design/app?rev=1-4E2`](https://docs.couchdb.org/en/stable/api/ddoc/common.html#put--db-_design-ddoc "PUT /{db}/_design/{ddoc}"))
    
- Deleting a design document ([`DELETE /database/_design/app?rev=2-6A7`](https://docs.couchdb.org/en/stable/api/ddoc/common.html#delete--db-_design-ddoc "DELETE /{db}/_design/{ddoc}"))
    
- Triggering compaction ([`POST /database/_compact`](https://docs.couchdb.org/en/stable/api/database/compact.html#post--db-_compact "POST /{db}/_compact"))
    
- Reading the task status list ([`GET /_active_tasks`](https://docs.couchdb.org/en/stable/api/server/common.html#get--_active_tasks "GET /_active_tasks"))
    
- Restarting the server on a given node ([`POST /_node/{node-name}/_restart`](https://docs.couchdb.org/en/stable/api/server/common.html#post--_node-node-name-_restart "POST /_node/{node-name}/_restart"))
    
- Reading the active configuration ([`GET /_node/{node-name}/_config`](https://docs.couchdb.org/en/stable/api/server/configuration.html#get--_node-node-name-_config "GET /_node/{node-name}/_config"))
    
- Updating the active configuration ([`PUT /_node/{node-name}/_config/{section}/{key}`](https://docs.couchdb.org/en/stable/api/server/configuration.html#put--_node-node-name-_config-section-key "PUT /_node/{node-name}/_config/{section}/{key}"))
```