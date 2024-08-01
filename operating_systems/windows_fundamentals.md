# Windows fundamentals

## History

- Microsoft Windows is a group of several graphical operating system families, all of which are developed, marketed, and sold by Microsoft.

- 1st version of Windows was released in 1985 as a GUI add-on to MS-DOS.

- Windows 95 was the first version of Windows with a Start menu, taskbar, and typical Windows desktop interface we still use today.

## Versions of windows

- Windows 1.0 (1985)
- Windows 2.0 (1987)
- Windows 3.0 (1990)
- Windows 3.1 (1992)
- Windows 95 (1995)
- Windows 98 (1998)
- Windows ME (2000)
- Windows XP (2001)
- Windows Vista (2006)
- Windows 7 (2009)
- Windows 8 (2012)
- Windows 8.1 (2013)
- Windows 10 (2015)


## Note

- Linux tool called `xfreerdp` can be used to connect to a Windows machine using RDP protocol.
- Syntax for the command is : `xfreedp /v:<targetIP> /u:<username> /p:<password>`

## OS Structure

- In Windows OS, root directory is <drive_letter>:\ (usually C drive.)
- The directory structure of the boot partition / root directory is as follows :

    - Perflogs : Can hold windows performance logs but is empty by default
    - Program Files : On 32-bit systems, 16-bit and 32-bit programs are installed here. On 64-bit systems, only 64-bit programs are stored here.
    - Program Files(x86) : 32-bit and 16-bit programs on 64-bit system are installed here.
    - ProgramData : This is a hidden folder that contains data that is essential for certain installed programs to run. This data is accessible by the program no matter what user is running it.

    - Users : This folder contains user profiles for each user that logs into the system and contains two folders Public and Default.

    - Default : This is the default user profile template for all created profiles. Whenever a new user is added to the system, their profile is based on the Default profile.

    - Public : This folder is intended for computer users to share files and is accessible to all users by default.

    - AppData : Per user app data and settings are stored in a hidden user subfolder. Each of these folder contains three subfolders : 
        - Roaming : This folder contains machine-independant data that should follow the user's profile, such as the custom dictionaries.

        - Local : This folder is specific to the computer itself and is never synchronized across the network.

        - LocalLow : It is similar to Local but it has a lower data integrity level. Therefore, it can be used, for example, by a web browser set to protected or safe mode.

    - Windows : The majority of the files required by Windows OS are contained here.

    - System, System32, SysWOW64 : Contains all DLL required for the core features of Windows and the Windows API. The OS searches these folders any time a program asks to load a DLL without specifying a specific path.

    - WinSxS : The Windows Component Store contains the copy of all Windows components, updates and service packs.


## File Systems

- There are 5 types of Windows file systems: FAT12, FAT16, FAT32, NTFS and exFAT.
- FAT12 and FAT16 are no longer used by the modern Windows OS.

### FAT32

- FAT32 (File Allocation Table) is widely used in many devices like USBs and SD cards.
- The 32 is the name refers to the fact that FAT32 uses 32 bits of data for identifying data clusters on a storage device.

- Pros of FAT32 includes : 
    - Device Compatibility
    - OS Compatibility , because both Linux and macOS supports this file type

- Cons of FAT32 includes :
    - Can only be used with files that are less than 4GB.
    - No built-in data protection or file compression features.
    - Must use third-party tools for file encryption,


### NTFS

- NTFS stands for New Technology File System
- It is the default windows file system since Windows NT3.1

- Pros of NTFS includes :

    - Reliable and can restore the consistency of the file system in the event of a system failure or power loss.
    - Secure by allowing granting permissions on both files and folders.
    - Supports very large-sized partitions.
    - Has journaling built-in, meaning that file modifications are logged.

- Cons of NTFS includes :

    - Most mobile devices do not support NTFS natively.
    - Older media such as TVs and digital camera do not support NTFS.

    Get-WmiObject -Class Win32_OperatingSystem | select SystemDirectory,BuildNumber,SerialNumber,Version | ft