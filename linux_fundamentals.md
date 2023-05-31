# Linux fundamentals

## Introduction

- Linux was a project started by Finnish student named Linus Torvalds.
- Linux has over 600 distributions, some popular ones being Ubuntu, Debain, Fedora, OpenSUSE, Redhat and others.

## Principles

### Everything is a file

- All config files for various services running on linux are stored in one or more text files.

### Small, single purpose programs

- Linux offers many tools , with each tool doing only one job.

### Configuration data stored in files

- /etc/passwd contains all the user data that are registered in the system

## Components

### BootLoader

- A piece of code that runs the guide to boot the operating system.
- GRUB is very popular

### OS Kernel

- Main component of an operating system.
- It manages the resources for system's I/O devices at hardware level

### Deamons

- Background services are called deamons in linux.
- Their purpose is scheduling, printing etc.

### OS Shell

- The OS shell or CLI is the interface between user and the system.
- Most commonly usees shells are Bash, zsh, Tcsh/Csh, Fish.

### Graphics server

- provides graphical sub-system called X or 'X' system that allows graphical programs to run locally or remotely on X-windowing server.

### Windows Manager

- aka GUI.
- most common are GNOME, KDE, MATE, Unity and Cinnamon.

### Utilities

- Applications

## Linux File System Hierarchy

- / : Top level directory contains all the files required to boot the OS before other filesystems are mounted.
- /bin : Contains essential command binaries.
- /boot : Consists of the static bootloader, kernel executables, and files required to boot the OS.
- /dev : Consists of device files to facilitate access to every hardware device attached to system.
- /etc : Local system configuration files. Config files for installed apps may be saved here.
- /home : Each user on the system has a subdirectory here for storage.
- /lib : Shared library files that are required for system boot.
- /media : External removable media files such as USB devices are mounted here.
- /mnt : Temporary mount points for regular filesystem.
- /opt : Optional files such as third party tools can be saved here.
- /root : The home directory for the root user.
- /sbin : The directory contains executables used for system administration.
- /tmp : The OS and many programs use this directory to store temporary files. It is cleaned after reboot.
- /usr : Contains executables, libraries, man files etc.
- /var : containes variable data files such as log files, email in-boxes, web applications related files and more.


## Getting help from the shell

- Two ways to get help from the shell are

    - Man pages : In man pages we find the detailed manuals with detailed explanations. 
        - Syntax : ```man <tool>```

    - Help  functions : We can look at the optional parameters without browsing through the complete documentation.
        - Syntax : ```<tool> --help```

## System information

- whoami : Displays the current username
- id : returns user id
- hostname : sets and prints the name of the host system
- uname : prints the basic information about the OS and system hardware
- pwd : returns present directory.
- ifconfig : used to assign or to view an address to a network interface or configure network interface parameters
- ip : manipulates routing, network devices, interfaces and tunnels.
- netstat : shows network status.
- ss : investigates sockets.
- ps : shows process status.
- who : displays who is logges in.
- env : prints the environment or sets and executes the command.
- lsblk : lists block devices.
- lsusb : lists usb devices
- lsof : lists opened files.
- lspci : lists PCI devices.

### Some tips about above commands

- id command can be used by the pen testers to see what access the user has.
- Running uname -a command prints all the information about the machine in a specific order.
- ls -i returns the index of files and directories

## Secure Shell (SSH)

- Secure shell is a protocol that allows clients to access and execute commands or actions on remote computers. 
- SSH is preferred choice for many admin to configure and maintain a computer through remote access.
- We can connect to a remote computer using this command : 
``` ssh [username]@[IP address] ```

## Files and Directories

- touch : create an empty file
- mkdir : create an empty directory
- mv : moves and also renames the files and directories.

## Editing Files

Some linux based text editors are : 

### Editors

- Nano
- Vi
- Vim
- Gedit

### Nano

- Create a new file using the syntax : 
    ``` nano [filename] ```

- Here a caret(^) stands for Ctrl key
- Ctrl + W : Search
- Ctrl + 0 : Confirms the filename and saves the file
- Ctrl + X : leaves the editor

### VIM 

- Open source
- Improved clone of Vi editor.
- Vim offers six fundamental modes that makes our work easier : 
    - Normal : All inputs are considered as editor commands. So there is no insertion of entered   characters into the editor buffer. Normal mode is default.
    - Insert : With a few exceptions, all entered characters are inserted into the buffer.
    - Visual : It is used to mark a contiguous part of the text, which will be visually highlighted. By positioning the cursor, we change the selected user. The highlighted area can then be edited in various ways, such as deleting, replacing.
    - Command : It allows us to enter single line commands at the bottom of the editor. This is used for sorting, replacing text sections or deleting them.
    - Replace : The newly entered text will override existing text characters unless there as no more old characters.
- We can close vim by first going to command mode using ":" then typing q for exiting the editor.
- Vim offers vimtutor to excel in vim editor.

## Find Files and Directories'

### Which 

- This tool returns the path to the file or link that should be executed. 
- Syntax : 
    ``` which [name] ```

- If the file does not exist, no results will be displayed

## Find

- Besides searching , find tool can filter the results too.
- Filters like size of file. 
- Syntax : 
    ``` find <location> <options> ```

- One example is :
    ``` find / -type f -name *.conf -user root -size +20k -newermt 2020-03-03 -exec ls -al {} \; 2>/dev/null ```

    - -type f : We define the type of searched object, f stands for file
    - -name *.conf : we indicate the name of the file.
    - -user root : sets to filter all the files with user as root.
    - -size +20k : filter all the located files and specifiy the min size of the file to 20kb
    - -newermt 2020-03-03 : Only files newer than specified date are shown.
    - -exec ls -al {} \; : This option executes the specified command, using the curly brackets as placeholders for each result. The backslash escapes the next character from being interpreted by the shell, otherwise the semicolon would terminate the command.
    - 2>/dev/null : This is STDERR redirection to null device. It ensures error handling.


### Locate 

- locate works with a local database that contains all the information about existing files and folders.
- We can update the database using following command : 
    - ``` sudo updatedb ```
- locate does not have much filters
- it is faster and hence recommended.

## File Descriptions and redirections

### File Descriptors

- A file descriptor (FD) is an indicator of connection maintained by kernel to perform I/O operations
- In windows, it is called filehandle.
- By default, the first three file descriptors in linux are : 

    - Data stream for Input - STDIN
    - Data stream for Output - STDOUT
    - Data stream for output that relates to an error - STDERR

- STDIN and STDOUT

    - The input we give to any command is STDIN and the output is STDOUT

- Redirect STDOUT to a file
    - Use ">" sign to redirect
    - Example : 
        - ``` find /etc/ -name shadow 2>dev/null > results.txt ```

- Redirect STDOUT and STDERR to seperate files
    - We use FD numbers (1 for out and 2 for err) to redirect them
    - Example : 
        - ``` find /etc/ -name shadow 2>stderr.txt 1>stdout.txt ```

- Redirect STDIN 
    - The < and > signs can be seen as directions in form of arrow that tells us "from where" and "where to" the data should be redirected.
    - Example : 
        - ``` cat < stdin.txt ```

- Redirect STDOUT and append file
    - We use >> sign to append a file.

- Redirect STDIN Stream to file
    - >> sign can be used to add our standard input through a stream.
    - We can use EOF ( End of File ) function to define the input's end.
    - Example : 
        - ``` cat << EOF > stream.txt ```

### Pipes

- Pipes are another way to redirect inputs and outputs.
- One of the most commonly used tool is ``grep``
- Grep is used to filter STDOUT.
- Example : 
    - ``` find /etc/ -name *.conf 2>/dev/null | grep systemd ```
- We can use multiple pipes for many redirects


## Permission management

- You need execute permissions to traverse through a directory
- There are three permisions : 
    - Read
    - Write
    - Execute
- And we can set three types of users for any resource :
    - Owner
    - Group
    - Others

### Changing Permissions

- We can modify permissions using the ``chmod`` command.
- Syntax : 
    - ``` chmod a+x [filename] ```
- We can use octal values instead of strings too.

### Changing Owner

- Syntax : ``` chown <user>:<group> [file] ```

###  SUID and SGID

- We can configure special permissions for files by settings the Set User ID and Set Group ID bits.
- They allow the user to run programs with the rights of another user.
- Admin uses it to give their users special rights for certain applications or files.


### Sticky Bits

- These are types of file permissions in Linux that can be set on directories for extra security.
- It is used on directories that are shared my multiple users to prevent any user from deleting or renaming files in that directory.
- We can add a letter t in the execute permission.
- "T" means that all other users dont have execute permissions and therefore cannot see the contents of the folder nor run my programs. 
- "t" means that users have execute permissions.

## User management

Some common commands for user management in linux are : 

- sudo : Executes command as different user
- su : SU utility requests appropriate user credentials via PAM and switches that user ID
- useradd : creates a new user
- userdel : deletes a user and related files
- usermod : modifies the user details.
- addgroup : adds a group to the system.
- delgroup : deletes a group
- passwd : changes the password.

## Package management

- Packages are archives that contain binaries of software, config files and other dependencies.

- Some tools for package management are : 
    - dpkg : Tool to install , build, remove and manage .deb packages.
    - apt : command line package manager
    - aptitude : alternative to apt
    - snap : for snap packages. Snap has more security
    - pip : for python packages
    - git 

### Advanced Package Manager ( APT )

- Debian based Linux distributions use apt.
- Apt uses a database called apt-cache.
- This provides information about packages installed on our system offline.
- ``` apt list --installed ```
    - It lists all installed packages

## Service and process management

- There are two types of services : 
    - Internal : the relevant services that are required at system startup.
    - Daemons : Services that run on background, identified by "d" at the end of the program like systemd, sshd

- Most linux distributions use ``systemd``.
- This is an Init process started first and thus has process ID 1.
- This daemon monitors and takes care of the orderly starting and stopping of other services.
- Besides ``systemctl`` we can also use `` update-rc.d `` to manage SysV into script links.
- We can start a process using ``systemctl start [process] `` command
- we can see the status of any command using status option
- We can use ``ps`` tool to check the automatically running processes.
- ``systemctl list-units --type=service `` command lists all processes

### Processes

- A process can have following states : 
    - Running
    - Waiting
    - Stopped
    - Zombie ( stopped but still has an entry in the table )

- Processes can be controlled using kill, pkill, pgrep commands

- To background a process, there is a shortcut ``CTRL + Z``

### Executing multiple commands

- There are three possibilities to run several commands, one after the other. These are seperated by : 
    - Semicolon
    - Double ampersand characters (&&)
    - Pipes

## Task Scheduling

- systemd is the tool used to start any process or script at specified time.
- We can also specify the triggers that triggers the process.
- To do this, we need to take some steps and precautions before our scripts or processes are automatically executed by the system.
    - Create a timer
    - Create a service
    - Activate the timer

### Create a timer

- To create a timer, we need to create a directory where the timer script will be stored.

``` sudo mkdir /etc/systemd/mytimer.timer.d ```
