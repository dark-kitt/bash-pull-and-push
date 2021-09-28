# **bash - pull | push - macOS / Linux**

## Introduction

Bash `pull` | `push` script based on Rsync for `macOS` / Linux. With these scripts, you can sync local and remote directories via `SSH` connection. Exclude files or directories as a list (string) or as an `.ignore` file.

* default local directory is `/Workspace`.
* default remote directory is `/www`.

Change the default directories to your specific wish.

### Requirements

* Rsync
* macOS / Linux

## Global
If you want to use pull and push globally copy the shell scripts in the `user/local/bin/` directory. (macOS)

## Usage

**pull** < options > < user@host > < source > < file/directory >
```text
bash pull -e "./.ignore" user@127.0.0.1 ~/Worksapce /www
```
```text    
bash pull -WS -i "file-1.txt","file-2.txt" user@127.0.0.1 / /
```
```text
bash pull -h
    <options>
        -i              exclude list: \"file-1.txt\",\"file-2.txt\"
        -e              exclude file: \"./.ignore\" (default: ./.ignore)
        -W              upload directory starts with: /Workspace
        -S              source directory starts with: /www

    <user@host>
        example         SSH user name and IPv4 address: user_name@127.0.0.1

    <source>
        source     host source directory: /path/to/directory

    <file/directory>
        file            file path: /path/to/file.ext
        directory       directory path: /path/to/directory
```
**push** < options > < user@host > < file/directory > < destination >
```text
bash push -e "./.ignore" user@127.0.0.1 ~/Worksapce /www
```
```text
bash push -WD -i "file-1.txt","file-2.txt" user@127.0.0.1 / /
```
```text
bash push -h
    <options>
        -i              exclude list: \"file-1.txt\",\"file-2.txt\"
        -e              exclude file: \"./.ignore\" (default: ./.ignore)
        -W              upload directory starts with: /Workspace
        -D              destination directory starts with: /www

    <user@host>
        example         SSH user name and IPv4 address: user_name@127.0.0.1

    <file/directory>
        file            file path: /path/to/file.ext
        directory       directory path: /path/to/directory

    <destination>
        destination     host destination directory: /path/to/directory
```

Get help via `bash pull -h` or `bash push -h`.

---
---

## License

[![](https://upload.wikimedia.org/wikipedia/commons/d/d0/CC-BY-SA_icon.svg)](https://creativecommons.org/licenses/by-sa/2.0/)
