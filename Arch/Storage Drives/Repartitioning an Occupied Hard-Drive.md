# Repartitioning an Occupied Hard-Drive

## Cheatsheet   

- [ ] [**1.**]( #1-find-your-drive ) lsblk -f 
- [ ] [**2.**]( #2-make-mounting-directory ) sudo mkdir -p /mnt/yourdrive
- [ ] [**3.**]( #3-mount-your-drive ) sudo mount /dev/sdx# /mnt/yourdrive
- [ ] [**4.**]( #4-backup-your-files ) rsync -azvP --append-verify "/mnt/yourdrive/" "/path/to/backup/directory/"

## Purpose

This guide explains how to repartition or resize an internal/external hard-drive with pre-existing data on it.
Repartitioning hard-drives can be done for various reasons. Perhaps you want to multi-boot or use your old external hard-drive as 
a backup drive. Or maybe your entire disk got corrupted.

### 1. Find your drive 

First, find the used hard-drive you want to repartition by going into your terminal and typing:

`lsblk -f`

Use sudo, su, etc. before the command if denied permission.

`sudo lsblk -f`

The path to your external drive should be in the following format e.g.: /dev/sda1

### 2. Make mounting directory 

Create a /mnt folder to mount your hard-drive if you haven't done so. 

`sudo mkdir -p /mnt/yourdrive`

### 3. Mount your drive 

Mount your hard-drive:

`sudo mount /dev/sdx# /mnt/yourdrive`
x = 3rd letter of drive, # = number of partition

### 4. Backup your files with rsync

I recommend using **rsync** to backup your files. 

`rsync -azvP --append-verify "/mnt/yourdrive/" "/path/to/backup/directory/"`

**IMPORTANT:** Make sure " / " is at the end of each directory in the command. 
Otherwise, rsync will not detect your pre-existing files and will duplicate your files into a new subdirectory. 
Adding " / " at the end of each directory is called **Trailing.**

This command allows you to resume file-transfer in case it gets interrupted and shows the overall progress of your transfer.
In case you get interrupted just re-run the same command!

 - -a = archive mode, perserves permissions, timestamps, symlinks, etc. (like cp -a)
 - -v = verbose mode, details what files are being transferred
 - -z = compression mode, compresses your files during transfer. Helps with lowering bandwidth. 
 - -P = partial + progress mode, allows your files to be transferred as partial bits, great for resuming interrupted transfers. Progress shows an ETA (estimated time arrival) of file transfer completion. 
 - --append-verify = safest resume mode: appends missing data and checksums to resume backup from where interrupted. 

### 5. 

