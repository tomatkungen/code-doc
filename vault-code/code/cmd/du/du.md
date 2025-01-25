* **du** display disk usage statistics

```shell
# -h human readable like kb, MB, b
# -d <number> This limits the depth of the listing to one level down, meaning it will show the sizes of the immediate subdirectories only.

# Get the current size, total size is in the end of the output
$ du -h 
```

```shell
# Usage to drop folder size

# Navigate to a folder
$ cd Developer

# inside that folder
$ Developer/

# type
$ du -h -d 1

```