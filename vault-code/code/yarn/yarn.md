* [yarn pkg install](https://yarnpkg.com/getting-started/install)
* [yarn classic deprecated](https://classic.yarnpkg.com/en/docs/install#mac-stable)
* [Nodejs Corepack](https://nodejs.org/api/corepack.html)

```bash
# Install Package Node > v18
$ corepack enable

# Upgrade yarn
corepack install --global yarn@x.y.z

# Goto project package.json and that using yarn v1.22
$ corepack use yarn@* # sets the latest version in the package.json
# or package manager

$ corepack use pnpm@7.x # sets the latest 7.x version in the package.json
```

```bash
# Migrate npm package.json
$ corepack enable # if not already enabled
$ yarn set version berry
#Convert your `.npmrc` and `.yarnrc` files into [`.yarnrc.yml`](https://yarnpkg.com/configuration/yarnrc)
$ yarn install # migrage package
```

```shell
# Show yarn config v4.1.1
$ yarn config
```

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

```shell
# Uninstall yarn classic 1.22.5
$ brew uninstall --force yarn
$ npm uninstall -g yarn

$ yarn -v # still show version

# find the bin file
# /usr/local/bin/yarn
# rm /Users/<user>/.yarn/bin/yarn
which yarn 

$ rm /Users/<user>/.yarn/bin/yarn

yarn -v

$ rm -rf /usr/local/bin/yarn
$ rm -rf /usr/local/bin/yarnpkg
$ which yarn
```

```json
// Run Yarn in parallel or serial
{
    "parallel": "yarn script1 & yarn script2",
    "serial": "yarn script1 && yarn script2",
    "script1": "... some script here",
    "script2": "... some there script here"
}
```