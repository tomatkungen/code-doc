
```shell
// fuzzy search someone with *k*
git log --author="k"

// Fuzzy several authors
git log --author="\(tomat\)\|\(kim\)"

// Fuzzy several authors case insensitive
git log -i --author="\(tomat\)\|\(kim\)"
```