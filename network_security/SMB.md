# SMB

## Introduction

- SMB stands for Server Message Block.
- It is a communication protocol used for sharing files, printers, and other resources on a network.
- Request / Response protocol.
- Windows use SMB since Windows 95.

## Enumerating SMB

- There are SMB share drives, that can be connected to and used to view or transfer files.
- 1st step will be port scanning.
- Enum4Linux is a tool used to enumerate information from Windows machines or linux machines.
- Syntax is `enum4linux <ip> options`.

## SMB Exploits

- Remote code execution (RCE) vulnerabilities in SMB can allow attackers to execute arbitrary code on the target system.
- Like CVE-2017-7494.
- We have to use an SMB Client to exploit.
- We can remotely access using syntax ```smbclient //[IP]/[SHARE] -u [] -p []```.
- Anonymous access is also possible using the username as 'Anonymous' and not supplying a password.
