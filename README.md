# filename-extension-lists
Alphabetically sorted lists which can be used for `.gitignore` files or rsync's `--exclude-from=` parameter

## Example usage for `rsync` with `--exclude-from=`
### Exclude any `c` or `c++` compiled files
First merge and sort the desired files:
```bash
$ sort -um compiled/{c,c++} > /tmp/c_and_c++
```

Then copy the desired source to the destination:
```bash
$ rsync --archive --exclude-from=/tmp/c_and_c++ <src> <dest>
```
