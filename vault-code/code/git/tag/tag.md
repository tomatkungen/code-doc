* **Light weight** and **Annotated**

```shell
# List tag
git tag
```

```shell
# Create Annotated tag "git tag -a <version> -m <message>"
git tag -a v1.4 -m "my version 1.4"
git push

# Tag commits "git tag -a <version> <sha>"
git tag -a v1.2 9fceb02
git push
```

```shell
# Create Light weight tag
git tag v1.4-lw
git push
```

```shell
# Show commit sha to a tag
git show v1.4
```
