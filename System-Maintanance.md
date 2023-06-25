System Maintainance
-Compilea and Installl a package 
 - Ubuntu -> apt get source download 

 - apt install 'build-essential or yum groupinstall 'developmenttools'
mkdir compile 


Make and Install Programs from Sources
- download the linux Kernel 
- Tar -Jcf xz.tar.xz

Backup Operations
- dd tar and rsysnc
dd ->  is used to backing up devices to a file or another partition or devices, 
   **To work with partition you would want to unmount the mount point**
    dd  if=/dev/<device-name> of=/dev/<device-backup> 
    mount -t ext4 /dev/dev1 /mnt/point
- rsync -avz /source/directoryor-emote-fs 
