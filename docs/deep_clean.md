# Deep clean

the command yarn osd:clean will remove most of your workspace artifacts, but not all of them.  To perform a deep clean you need to also run:
```sh
find . -name 'target' -type d -prune -exec rm -rf '{}' +
```
