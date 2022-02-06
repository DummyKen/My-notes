# Notes from Coursera's Operating System and You: Becoming a Power User

## Directories in GUI and CLI
- Command Prompt
- Powershell(will be used in this course)

List
```ls C:\Users\```
List with hidden files shown
```ls -Force C:\ ```

## Linux Directory :)
I dont really have linux installed anywhere so I will just be looking and typing in imaginary bash. :) Oh I have WSL. Wont be the same but the commands will work at least.

To get the help with what each command does:
```linux
man ls
man rm
```
Listing directories in details:
```linux
ls -l filename/directory_name
```
Show all the files(including hidden) in the directory:
```linux
ls -a /
```
We can combine the commands as well:
```linux
ls -l -a /
```

## Absolute and relative paths
`Absolute` paths start from the main/home directory, whereas the `relative` starts from current directory.
```linux
>>cd /documents (Relative path)
>>cd C:/Users/Desktop/
```
- `pwd` for current working directory.
---
- To create a new folder with `space-included` name, use `:
```linux
(Creating a folder name my files)
mkdir my` files
```
- `history` command in powershell for history of commands. But wont use very often instead will use the `^`.

### Copying files & directories 
Most important part of my daily life :).
>Copying a txt file to `Desktop`
```linux
cp this.txt C:\Users\Desktop
```
>Copying all the `png` files into Desktop
```linux
cp *.png C:\Users\Desktop
```
### Moving and renaming files and directories
Changing the text files name
```linux
mv this.txt that.txt
```
Moving the file to desktop(*same command*)
```linux
mv this.txt ~\Desktop
```

### Removing files and directories
>Permanently removed
Removing `this.txt`
```linux
rm /this.txt
```
Removing `code_files` folder/directory:
```linux
rm /code_files
```
will ask if we're sure. To avoid that:
```linux
rm /code_files -recurse
```
and gone.

>And quiz coming up.

