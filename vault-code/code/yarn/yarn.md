
```shell
# Publish local package
yarn add file:./../git-nodejs-git-json/

```

```shell
# Update package version and add git tag if inside repo
yarn version --patch  # --minor | --major

git push --tags # push all tags to repo 

# Publish npm package
yarn publish
```