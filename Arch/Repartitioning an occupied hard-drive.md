# Repartitioning an occupied hard-drive

## Cheatsheet   

    1. [ ] Find your drive = lsdisk -f 
    2. [ ] Make directory = sudo mkdir -p /mnt/yourdrive
    3. [ ] Mount your drive = sudo mount /dev/hard-drive /mnt/yourdrive
    4. [ ] Backup files = rsync -av --progess /mnt/yourdrive /path/to/backup/directory

## Purpose

This guide explains how to repartition or resize an internal/external hard-drive with pre-existing data on it.
Repartitioning hard-drives can be done for various reasons. Perhaps you want to multi-boot or use your old external hard-drive as 
a backup drive. Or maybe your entire disk got corrupted.

## 1. Backup 

First step of priority is to make a backup of your files. Whether you are using an internal or external drive
the process should remain relatively the same.

### Backup 1.1

First, find the used hard-drive you want to use by going into your terminal and typing "lsdisk -f." Use sudo, su, etc. if denied permission.
The path to your external drive should be in the following format e.g.: /dev/sda1

Create a /mnt folder to mount your hard-drive if you haven't done so. e.g. "sudo mkdir -p /mnt/yourdrive"

Mount your hard-drive: "sudo mount /mnt/yourdrive /dev/sdx#" x = 3rd letter of drive, # = number of partition

### Backup 1.2 

I recommend using **rsync** to backup your files. Simply use 'rsync -av --progress /mnt/yourdrive /path/to/backup/directory'
This command will allow you to see the overall progress of files being transferred as well as an ETA (Estimated Time Arrival).

**Note: in case your transfer gets interrupted and you don't want to overwrite your pre-existing files use:** 
'rsync -av --progress --partial --append-verify /mnt/yourdrive /path/to/backup/directory'

- -a = archive mode, perserves permissions, timestamps, symlinks, etc. (like cp -a)
- -v = verbose mode, details what files are being transferred
- --progress = shows ETA and number of bytes being transferred
- --partial = keeps partially transferred files instead of deleting them
- --append-verify = safest resume mode: appends missing data and checksums to make sure nothing got corrupted.

### Backup 1.3 

