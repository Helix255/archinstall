Arch Basic Install Commands-Script
In this repository you will find packages-scripts for the base install of Arch Linux and the Gnome, KDE, Cinnamon and Xfce desktop environments. More to come for Windows Managers soon.
Modify the packages to your liking, make the script executable with chmod +x scriptname and then run with ./scriptname.
A script for the base install on MBR/Legacy will be available soon.
Remember that the first part of the Arch Linux install is manual, that is you will have to partition, format and mount the disk yourself. Install the base packages and make sure to inlcude git so that you can clone the repository in chroot.
A small summary:

If needed, load your keymap
Refresh the servers with pacman -Syy
Partition the disk
Format the partitions
Mount the partitions
Install the base packages into /mnt (pacstrap /mnt base linux linux-firmware git vim intel-ucode (or amd-ucode))
Generate the FSTAB file with genfstab -U /mnt >> /mnt/etc/FSTAB
Chroot in with arch-chroot /mnt
