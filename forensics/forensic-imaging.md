# Forensic Imaging

## Introduction

- Process of creating and exact, bit by bit copy of digital storage media.

- It ensures all data, including deleted files, hidden files and unallocated space is captured.

- Primary goal is to create a reliable copy for investigation and legal proceedings.

## Write blockers

- Hardware devices that prevent data from being written to the original storage media.

- Ensures that the original data is not altered during the imaging process.

- Write blockers are essential to maintain the integrity of the evidence.

## Audit Trails

- Detailed logs of all actions taken during the imaging process.

- Includes information such as the date and time of the imaging process, the device being imaged, and the name of the investigator.

- Audit trails are essential for maintaining the chain of custody and ensuring the integrity of the evidence.

## Creating a forensic image

### Tools

- dd : Standard Unix utility for copying and converting files, often used for creating raw disk images.

- dc3dd : Enhanced version of dd with additional forensic imaging features like hashing.

- ddrescue : Data recovery tool that effeciently copies data from damaged drives.

- FTK imager : GUI based tool for creating imgaes.

- EWF Tools (ewfacquire) : Tools for creating and handling Expert Witness Format(EWF) images.

### CMD 

- `sudo dc3dd if=/dev/loop10 of=example1.img log=imaging_loop10.txt`

    - `if` : Indicates the file to be  copied.

    - `of` :    Indicates where we want to write the disk bytes.

    - `log` : Save the output into the file.

## Checking integrity

- The process uses crpytographic hash functions, such as MD5, SHA-1 to generate unique hash values for both data.

- By comparing the hashes we can check integrity of the original and copied files.

- Tools like `md5sum`, `sha1sum` can be used to generate hash values.

## Other types of imaging

- Remote Imaging : Involves creating images over the network, allowing it to acquire data without phyiscal access of device

- USB Imaging : Creating an image of USB drive's content

- Docker images : Creates snapshot of a docker container's filesystem and configuration.

