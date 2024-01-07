```shell
# Creates with preset npm setup for nx
npx create-nx-workspace@latest <organization name> --preset=npm
```

```shell
# install typescript in root level -W
npm i typescript -D -W
```

```shell
# Build will look for build script in package.json
npx nx build <foldername | packagename>
```

```shell
# Show graph in window
npx nx graph
```

```shell
# Build all project and dont use cache builds
npx nx run-many --target=build --skip-nx-cache
```

```shell
# inside a nx project you can list plugins
yarn nx list
```

```shell
# show all projects target
yarn nx show projects
```
