### Table of Contents

+ [Introducing the Shell](#introducing-the-shell)
+ [Navigating Files and Directories](#navigating-files-and-directories)
+ [Working with Files and Directories](#working-with-files-and-directories)
+ [Pipes and Filters](#pipes-and-filters)
+ [Loops](#loops)

# The Unix Shell

## Introducing the Shell


#### Questions:
- What is a command shell and why would I use one?

#### Notes:
- Graphical User Interface (GUI) versus Command Line Interface (CLI)
- Read-evaluate-print-loop (REPL)
- Command, flag, argument
- Flexibility and automation

#### Try

- [ ] `pwd`
- [ ] `ls -F /`

## Navigating Files and Directories

#### Questions:
- How can I move around on my computer?
- How can I see what files and directories I have?
- How can I specify the location of a file or directory on my computer?

#### Notes:
- File system hierarchy
- Current working directory
- Root directory
- Home directory
- `man` and `--help`
- Abosulute vs Relative path

#### Try:

- [ ] `ls`
- [ ] `ls -F`
- [ ] `ls --help`
- [ ] `man ls`
- [ ] `ls -j`
- [ ] `ls -l`
- [ ] `ls -R`
- [ ] `ls -F Desktop`
- [ ] `pwd`
- [ ] `cd desktop` or `cd Desktop`
- [ ] `cd data-shell`
- [ ] `cd data`
- [ ] `cd ..`
- [ ] `cd ~/desktop/data-shell/data` or `cd ~/Desktop/data-shell/data`
- [ ] `cd /`
- [ ] `cd ~`
- [ ] `cd -`

#### Activity:

- [ ] move into `data-shell` directory
- [ ] enter the command `ls north-pacific-gyre/2012-07-03/` using tab completion

### Working With Files and Directories


#### Questions:
- How can I create, copy, and delete files and directories?
- How can I edit files?

### Notes
- Naming conventions for files and directories
- The Nano text editor
- Deleting with `rm` is forever

### Try
- [ ] Go back to `data-shell` by checking where you are `pwd`and using `cd`
- [ ] Check what's in `data shell` with `ls -F`
- [ ] Make a new directory called 'thesis' `mkdir thesis`
- [ ] Check what's in the directory again `ls -F`
- [ ] Nothing is in `thesis` because it's brand new. Check with `ls -F thesis`
- [ ] Move into `thesis` with `cd thesis`
- [ ] Use Nano to add and edit a file `nano draft.txt`. Add some lines of text, then use __Ctrl-X__ to exit.
- [ ] Go to your home directory and make a file using touch. `cd ~` followed by `touch my_file.txt`
- [ ] Use `ls -l` to inspect the files. How large is `my_file.txt`? Why?
- [ ] Move back into `thesis` in `data-shell` with `cd` and remove the draft file with rm `rm draft.txt` using tab completion. But be careful!
- [ ] Run `ls` to see if the file is still there.
- [ ] Re-add the file and move back into `data-shell` with `nano draft.txt`, `ls`, and `cd ..`
- [ ] Try removing `thesis` with `rm thesis`. What happens?
- [ ] Type out `rm -r thesis` for removing the directory recursively. But don't hit enter! We're not ready to delete it yet.
- [ ] Instead try removing the directory safely with `rm -r -i thesis`. Type `y` for each file to delete.
- [ ] Make the `thesis` directory in `data-shell`again by checking where you are `pwd`and using `mkdir thesis`
- [ ] Remake the file `draft.txt` with nano `nano thesis/draft.txt`
- [ ] Change the filename of `draft.txt` to `quotes.txt` using `mv thesis/draft.txt thesis/quotes.txt`
- [ ] Check what happened with `ls thesis`
- [ ] Move `quotes.txt` into the current working directory with `mv thesis/quotes.txt .`
- [ ] See what's in `thesis` with `ls thesis`
- [ ] Find `quotes.txt` in the current working directory with `ls`






## Pipes and Filters


#### Questions:
- How can I combine existing commands to do new things?




## Loops


#### Questions:
- How can I perform the same actions on many different files?



> __Full Tutorial:__ <https://swcarpentry.github.io/shell-novice/>
