* **Light weight** and **Annotated**

```shell
# List tag
git tag
```

```shell
# Create Annotated tag "git tag -a <version> -m <message>"
git tag -a v1.4 -m "my version 1.4"
git push --tags# git push origin <tag_name>

# Tag commits "git tag -a <version> <sha>"
git tag -a v1.2 9fceb02
git push --tags # git push origin <tag_name> | git push origin --tags

```

```shell
# Create Light weight tag
git tag v1.4-lw
git push # git push origin <tag_name> | | git push origin --tags
```

```shell
# Create feature branch with tag "git checkout -b <branch_name> <version>"
git checkout -b feture/main-branch v1.0.0
```

```shell
# Show commit sha to a tag
git show v1.4
```
