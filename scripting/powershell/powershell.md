# Powershell

## Introduction

- Powershell is the tool for task automation and configuration management.
- Built on .NET framework.
- Object oriented, i.e. it can handle complex data types and interact with system components more effectively.
- Initially for windows, now crossplatform.

## History

- Limitations of cmd.exe in automating and managing the systems.
- Needed a tool to interact with windows APIs and do more complex tasks.
- Powershell released in 2006, by Jeffrey Snover.
- Powershell core, i.e. cross platform version was launched in 2016.

## Syntax

- Powershell syntax contains `cmdlets`. They are more powerful than traditional windows commands.
- Naming convention used by cmdlets are `Verb-Noun`. Here Verb describes the action, Noun specifies the object on which action is performed.

## Basic Cmdlets

- `Get-Command` - List all available cmdlets, functions, aliases, and scripts.
  - You can filter commands by their properties of their objects
  - `Get-Command -CommandType "Function` - Gets only functions.
- `Get-Help` - Provides detailed information about cmdlets, including usage, parameters, and examples.
  - Paramters like `-examples` `-detailed` `-full` `-online` expands the cmdlet.
- `Get-Alias` - Lists all available aliases.
- `Find Module` - Searches for additional cmdlets in online repository.
  - `-Name` - If the whole name is not known, this parameter helps search by keywords.
- `Install-Module` - Installs the cmdlets from online repository.

## Navigating File Systems

- `Get-ChildItem` - Lists files and directories in a location specified with `-Path` parameter.
- Gives current directory path as default.
- `Set-Location` - Navigates to a specified directory.
- `New-Item` - Creates a new item, `-ItemType` specifies the type as directory or file.
- `Remove-Item` - Removes both directories and files.
- `Copy-Item` - Copies or moves files and directories alike. Use `Move-Item` for moving.
- `Get-Content` - Read and displays the contents of a file specified with `-Path` parameter.

## Piping, Filtering and Sorting

- Piping is a technique used in CLI environments that allows output of one command to be used as input of another command.
- Represented by | symbol.
- In powershell, piping passes objects instead of text to the next command. Objects carry properties and methods also with them.
- `Where-Object` cmdlet can be used to advanced data filtering and manipulation.
- Comparison operators can be used by using parameters like `-ne` or `-eq` with above command.
- `Select-Object` is used to select specific properties from objects or limit the number of objects returned.
  - For example, `Get-ChildItem | Select-Object Name,Length` - gives only name and length of the object.
- `Select-String` - Searches for string patterns in the files, like `grep` or `findstr` in windows. Supports regex.

## System and Network Information

- `Get-ComputerInfo` - Retrieves comprehensive system information.
- `Get-LocalUser` - Lists all local user accounts on the system.
- `Get-NetIPConfiguration` - Similar to `ipconfig` gets details about network interfaces in the system.

## Real time system analysis

- `Get-Process` - Provides the detailed view of all currently running processes, including CPU and memory usage.
- `Get-Service` - Retrieves the information about the status of services on the machine, used for troubleshooting.
- `Get-NetTCPConnection` - Monitor active network connections, displays current TCP connections, giving insights into both local and remote endpoints. Used in incident response and malware analysis, as it uncovers hidden backdoors or established connections.
- `Get-FileHash` - Helps verify the file integrity and detect potential tampering.

## Scripting

- Process of writing and executing a series of commands contained in a text file, known as a script, to automate tasks that one would generally perform manually.
- `Invoke-Command` - Enables remote management and combining it with scripting, automates the tasks. We can execute any command with this cmdlet. Even in remote systems.
