# Repartitioning an Occupied Hard-Drive

## Cheatsheet   

- [ ] [**1.**]( #1-find-your-drive ) lsblk -f 
- [ ] [**2.**]( #2-make-mounting-directory ) sudo mkdir -p /mnt/yourdrive
- [ ] [**3.**]( #3-mount-your-drive ) sudo mount /dev/sdx# /mnt/yourdrive
- [ ] [**4.**]( #4-backup-your-files ) rsync -av --progess --partial --append-verify /mnt/yourdrive/ /path/to/backup/directory/

## Purpose

This guide explains how to repartition or resize an internal/external hard-drive with pre-existing data on it.
Repartitioning hard-drives can be done for various reasons. Perhaps you want to multi-boot or use your old external hard-drive as 
a backup drive. Or maybe your entire disk got corrupted.

### 1. Find your drive 

First, find the used hard-drive you want to repartition by going into your terminal and typing "lsblk -f." Use sudo, su, etc. if denied permission.
The path to your external drive should be in the following format e.g.: /dev/sda1

### 2. Make mounting directory 

Create a /mnt folder to mount your hard-drive if you haven't done so. e.g. "sudo mkdir -p /mnt/yourdrive"

### 3. Mount your drive 

Mount your hard-drive: "sudo mount /dev/sdx# /mnt/yourdrive"
x = 3rd letter of drive, # = number of partition

### 4. Backup your files with rsync

I recommend using **rsync** to backup your files. Simply use 'rsync -av --progress /mnt/yourdrive/ /path/to/backup/directory/'

**IMPORTANT:** Make sure " / " is at the end of each directory in the command. 
Otherwise, rsync will not detect your pre-existing files and will duplicate your files into a new subdirectory. 
Adding " / " at the end of each directory is called **Trailing.**

This command will allow you to see the overall progress of files being transferred as well as an ETA (Estimated Time Arrival).

**Note: in case your transfer gets interrupted and you don't want to overwrite your pre-existing files use:** 

{ rsync -av --progress --partial --append-verify /mnt/yourdrive /path/to/backup/directory } 
 - -a = archive mode, perserves permissions, timestamps, symlinks, etc. (like cp -a)
 - -v = verbose mode, details what files are being transferred
 - --progress = shows ETA and number of bytes being transferred
 - --partial = keeps partially transferred files instead of deleting them
 - --append-verify = safest resume mode: appends missing data and checksums to resume backup from where interrupted. 

### 5. 

