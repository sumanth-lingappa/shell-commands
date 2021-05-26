# shell-commands
My experiments with shell commands

## check if all the functions in a file is correctly passed with arguments (dirty way)

```zsh
for func in `grep "def " <filename> | cut -c 5- | cut -d '(' -f 1`;
do
grep "$func(" <filename>
echo "-----------------"
done
```
