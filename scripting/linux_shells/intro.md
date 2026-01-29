# Linux Shells

- Bash is the default shell for most linux distros.

## Basics

- `cd` - Change directory
- `pwd` - Present working directory.
- `ls` - Lists children.
- `cat` - Displays file content.
- `grep` - Searching in a file.

## Types of Linux Shells

- `echo $SHELL` - Gives the type of shell you are using.
- `/etc/shells` contains all installed shells in linux system.
- `chsh -s /usr/bin/zsh` - permanently changes the default shell to specified shell. zsh here.

### Bourne Again Shell (Bash)

- Default shell for most of the linux distributions.
- Offers a tab completion feature, keeps a history of commands used.
- Borrows features and functionalities from all older shells like sh, ksh and csh.

### Friendly Interactive Shell (Fish)

- More user-friendly than other shells.
- Offers very simple syntax
- Has auto-spell correction feature.
- More customizable.
- Provides tab completion, scripting and command history features.

### Z Shell (zsh)

- Considered a modern shell.
- Tab completion and scripting
- Spell correction and extensive customizability.

## Shell scripting

- Extension `.sh` used for scripts.
- Every script starts from shebang. It is a combination of some characters that are added at the beginning of the script, starting with `!#` followed by the name of the interpreter to use while executing the script.

### Variables

- `read name` - read takes input from the user, and stores it in the variable name.
- `echo` - displays to the user, outputs.

### Loops

- `for` - for loop iterates over a set of data as per the rule specified. `do` indicates the start of the loop and `done` indicates the end of the loop.

### Conditional statements

- `if then else fi` statements are used for conditional scripting statements.
