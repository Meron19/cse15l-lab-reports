# Lab Report 3 - Researching Commands

In this lab report, you will learn about using the `find` command used in the command-line and some options that can be used with this command.

---

## Part One: Command `find` With `-name` Option

Below is the command-line command used to search and find all the files based on the name within the current working directory and the output of resulting from using the command.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -name "*.md"
./example.md
./README.md
```

Using the `find` command with this option allows me to find all the files of a certain file type. This can be helpful is aiding me to quickly locate what file I may be looking for. In this case, using the command allowed me to find all the files with the type `.md` in my current working directory, which were only two files.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -name "*results*" 
./find-results.txt
./file-results.txt
./grep-results.txt
```

The `find` command with the option above uses the same method of searching the current working directory for all the files with the same name, but, in the case of this command-line, using stars before and after a specific word will indictate that you want to find all the files that contain that word as part of their name. In this case, I searched for all the files that have the word **results** and 3 files were returned as a result.

## Part Two: Command `find` With `-type` Option

Below is the command-line command used to search and find all the files based on the filetype within the current working directory and the output of resulting from using the command.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -type d
...
```

Using the `find` command with this option allows me to find all the files of the current directory. This can be helpful is aiding me to quickly locate what file I may be looking for. In this case, using the command allowed me to find all the files within my current working directory; however, for the sake of this site, I inputed the output as `...` because there are way too many files to even fit on this page.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -type f -empty 
./empty.txt
```

Here the `-type` option used in the `find` command searches for the file individually as compared to the previous command-line which searched through the directories. In this case, the command-line searched for all the files that were empty, which returned a single file that had no text or code.

## Part Three: Command `find` With `-exec` Option

Below is the command-line command used to search and find all the files based on the search citeria and it executes a given command in the file(s).

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -type d -empty -exec rmdir {} \;

find: ./empty: No such file or directory
```

Using the `find` command with this option first searches for all the files meeting the search citeria, in this case they just need to be an empty file. Then through the `-exec` option we can execute the remove directory command. This can be helpful is aiding me to quickly deleting unwanted directories or accessing and using the files within such directories.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -maxdepth 1 -name "*.md" -type f -exec rm {} \;
```

Here the `-type` option used in the `find` command searches for the file individually with the name containing `.md` in the current working directory and removes it. In this case, the terminal doesn't return anything but still executes the remove command, `rm`, and removes all the `.md` files in the current working directory, which were two in my case.

## Part Four: Command `find` With `-mtime` Option

Below is the command-line command used to search and find all the files based on the the time since the files have been modified.

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -mtime -7 
.
./empty.txt
./.git
./.git/objects
./.git/objects/04
./.git/objects/04/474a3237c11e32fd5e85c20b3cd5f3bbde626f
./.git/objects/04/3eb99393491241455746580f55306fa0ddcc84
./.git/objects/b3
./.git/objects/b3/537075783af46f636fc3c445d5eef6bd09df0c
./.git/objects/a5
./.git/objects/a5/bb2cd797f60f0a5d3f00d48fe393e016a3afb4
./.git/objects/e4
./.git/objects/e4/79486c2534d112d573f19742c59ca1cb75e3a2
./.git/objects/fb
./.git/objects/fb/a87f3ee9cfda8aaf35e7b266d58414843e474d
./.git/objects/20
./.git/objects/20/440e45e6f6944dc6cf2aa08b12ca49c1be1dda
./.git/objects/29
./.git/objects/29/d35ac26fa480bb91a686116d8c22e75ed5a9be
./.git/objects/91
./.git/objects/91/73e9956c4321ae696dae453f032383b52c5d0d
./.git/objects/06
./.git/objects/06/00a2f1adf3a50548ff3331271e0ba28c07d03f
./.git/objects/bf
./.git/objects/bf/6fd8b075aacf234523deae7577b69354b9e91a
./.git/objects/b1
./.git/objects/b1/af8c549174b0693766e884b81aa1c7d963edc7
./.git/objects/e6
./.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391
./.git/objects/1b
./.git/objects/1b/1cae261e08e48099c46c817112d7297191a31a
./.git/objects/71
./.git/objects/71/3141ac6f1975bb2ed9d78a32a60a919d531028
./.git/objects/49
./.git/objects/49/b8af5641bcde1a99297f727c26180e63b573b0
./.git/logs/HEAD
./.git/logs/refs/heads/main
./.git/logs/refs/remotes/origin
./.git/logs/refs/remotes/origin/HEAD
./.git/logs/refs/remotes/origin/main
./.git/logs/refs/remotes/upstream/HEAD
./.git/refs
./.git/refs/heads
./.git/refs/heads/main
./.git/refs/remotes/origin
./.git/refs/remotes/origin/HEAD
./.git/refs/remotes/origin/main
./.git/refs/remotes/upstream
./.git/refs/remotes/upstream/HEAD
./.git/index
./.git/COMMIT_EDITMSG
./.git/FETCH_HEAD
```

**Input & Output:**

```Java
meron@Merons-MacBook-Air docsearch % find . -mtime +7
...
```

Using the `find` command with this option searches for all the files based on the modification time given by the command, in this case 7 days. The only difference between the two command is the `-7` and `+7`. The plus and minus differientiate between if the files have not been modified versus have been modified within the modification date, respectively. This can be helpful is aiding me to quickly to narrow down where work has been done on the files and which files are left untouched. In the case of the second use of the command with the `-mtime` option, for the sake of this site, I inputed the output as `...` because there are way too many files to even fit on this page.
