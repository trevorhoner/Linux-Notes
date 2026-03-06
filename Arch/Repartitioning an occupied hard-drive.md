# Repartitioning an occupied hard-drive

## Backup 

First step of priority is to make a backup of your files. Whether you are using an internal or external drive
the process should remain relatively the same.

### Backup.1

First, find the used hard-drive you want to use by going into your terminal and typing "lsdisk -f." Use sudo, su, etc. if denied permission.

Create a /mnt folder to mount your hard-drive if you haven't done so. e.g. "sudo mkdir -p /mnt/yourdrive"

Mount your hard-drive: "sudo mount /mnt/yourdrive /dev/sdx#" x = 3rd letter of drive, # = number of partition

### Backup.2 

Navigate to your mounted hard-drive i.e. "/mnt/yourdrive" using a file-explorer or the "cd" command in terminal

The most straight forward way is use the "cp" command. e.g. "sudo cp -v /mnt/yourdrive /path/to/copy/directory."
'-v' = verbose, tells you what is being copied in realtime.

If you are using "nnn," type "a" to select all. Navigate to your copy destination and press: "ctrl + p"
