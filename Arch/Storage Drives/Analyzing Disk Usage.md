# Analyzing Disk Usage

## Cheatsheet

- [ ] [**1.**]( #1-install-ncdu ) sudo pacman -S ncdu
- [ ] [**2.**]( #2-analyze-disk-with-ncdu ) sudo ncdu -x /

## Purpose

Sometimes our disks can balloon or grow exponentially due to unintended backups from external drives. Or we just have too much fun downloading and installing files. Analyzing or checking your disk usage is important, because you can see how effectively you are managing your drives file storage.

### 1. Install ncdu

'sudo pacman -S ncdu' 
ncdu stands for **NCurses Disk Usage.** It's an extremely light-weight and fast application for analyzing disk space usage of Linux/Unix systems.

### 2. Analyze Disk with ncdu

'sudo ncdu -x /'
- sudo = gives root permission
- ncdu = NCurses Disk Usage
- -x = excludes all other directories besides what is being scanned
- " / " = the drive or directory to be analyzed
