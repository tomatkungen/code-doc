* https://jsr.io/ - homepage

```shell
# Add jsr cli package to package json
$ yarn add -D jsr
```

```shell
# add a package to project
$ npx jsr add @luca/cases

# add .npmrc file and add (usally added by default when run above)
@jsr:registry=https://npm.jsr.io
```

```

##### How to create and publish package
1. Goto jsr.io
2. login with user
3. upper left corner click profile picture
4. menu appers click publish package
5. pick scope "@myscope" and write package name "my-package"
6. paste config into local environment 
```

```shell
// jsr.json / deno.json
{
  "name": "@myscope/my-package",
  "version": "1.0.0",
  "exports": "./mod.ts" // point at entry file
}
```
7. run in terminal "npx jsr publish" or "yarn dlx jsr publish"
8. Redirected to github login
9. Redirected to jsr package manager
10. done
