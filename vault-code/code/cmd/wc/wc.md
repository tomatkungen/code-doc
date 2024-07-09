* Word count command

```shell
# count words in file
wc -l <textfile>

# or pipeline
<file | command> | wc -l

# example
git log --oneline | wc -l
```