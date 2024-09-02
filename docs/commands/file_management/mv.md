# `mv` Command

## Description
The `mv` (move) command is used to move or rename files and directories in Linux. It can move files to a different directory, rename files or directories, or both simultaneously.

## Syntax
```bash
mv [options] source destination
```
- **`source`**: The file or directory you want to move or rename.
- **`destination`**: The location where you want to move the file or directory, or the new name you want to give it.

## Options
`-i`: Interactive mode, prompts before overwriting an existing file.
`-f`: Force the move by overwriting any existing files without prompting.
`-n`: No-clobber, prevents overwriting of existing files.
`-v`: Verbose mode, displays a message for each file or directory moved.

## Examples
### Basic File Move
To move a file from one directory to another:
```shell
mv file.txt /home/user/documents/
```
This command moves `file.txt` to the `/home/user/documents/` directory.

### Rename a File
To rename a file:
```shell
mv oldname.txt newname.txt
```
This command renames `oldname.txt` to `newname.txt`.

### Move and Rename a File Simultaneously
To move a file to a new directory and rename it:
```shell
mv file.txt /home/user/documents/newfile.txt
```
This command moves `file.txt` to the `/home/user/documents/ directory and renames it to `newfile.txt`.

### Move a Directory
To move an entire directory:
```shell
mv /home/user/old_directory /home/user/new_directory
```
This command moves `old_directory` to `new_directory`.

### Interactive Mode
To prompt before overwriting files:
```shell
mv -i file.txt /home/user/documents/
```
You will be asked for confirmation before any existing file in the destination is overwritten.

### Force Overwrite
To move a file and overwrite any existing files without prompting:
```shell
mv -f file.txt /home/user/documents/
```
This command forces the move, replacing any files with the same name in the destination.

### Verbose Mode
To display each move operation:
```shell
mv -v file.txt /home/user/documents/
```
## Example Output
```shell
'file.txt' -> '/home/user/documents/file.txt'
```
### Prevent Overwriting
To move a file without overwriting an existing file:
```shell
mv -n file.txt /home/user/documents/
```
If a file with the same name exists in the destination, it will not be overwritten.

## Tips
- The `mv` command is powerful for reorganizing files and directories, especially when combined with options like `-i` and `-f` to control overwriting.
- Always use the `-i` option if you want to avoid accidental data loss due to overwriting.
- Remember that if the source and destination are on different file systems, `mv` might perform a copy and delete operation instead of a simple move.