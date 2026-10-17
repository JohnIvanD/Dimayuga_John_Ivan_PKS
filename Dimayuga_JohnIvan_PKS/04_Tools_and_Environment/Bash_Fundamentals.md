# Bash Fundamentals

[← Back to index](../README.md)

## Navigation and files
```bash
pwd                # current directory
ls -la             # list files (including hidden)
cd folder          # change directory
mkdir name         # create directory
touch file.txt     # create empty file
cp a b             # copy
mv a b             # move/rename
rm file            # delete
```

## Reading files
```bash
cat file.txt
head -n 5 file.txt
tail -n 5 file.txt
grep "word" file.txt
```

## Permissions
```bash
chmod +x script.sh
```

## Pipes and redirection
```bash
ls | grep ".md"
echo "text" > file.txt     # overwrite
echo "text" >> file.txt    # append
```

## Simple script
```bash
#!/bin/bash
name="Student"
echo "Hello, $name"
```

## My Reflection
I learned that Bash commands can be used to navigate directories, manage files, and perform tasks more efficiently through the terminal. This activity helped me become more familiar with command-line operations and understand their usefulness in Linux environments. I realized that practicing commands is important because small mistakes in syntax or file paths can affect the results. These skills are useful for system administration and cybersecurity tasks.

## Review Questions
1. Difference between `>` and `>>`?
2. What does `chmod +x` do?
3. What does a pipe (`|`) do?
