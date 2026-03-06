# Repartitioning an occupied hard-drive

## Safety

First step of priority is to make a backup of your files. Whether you are using an internal or external drive
the process should remain relatively the same.

### Safety.1

First, find the used hard-drive you want to use by going into your terminal and typing "lsdisk -f." Use sudo, su, etc. if denied permission.

Create a /mnt folder to mount your hard-drive if you haven't done so. e.g. "sudo mkdir -p /mnt/yourdrive"

Mount your hard-drive: "sudo mount /mnt/yourdrive /dev/sdx#" x = 3rd letter of drive, # = number of partition

### Safety.2 


