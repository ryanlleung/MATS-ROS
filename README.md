# MATS-ROS

## Installation with VirtualBox

Install ROS2 Humble on Ubuntu 22.04.1

Downlaod VirtualBox from https://www.virtualbox.org/wiki/Downloads
Download Ubuntu from https://ubuntu.com/download/desktop

Remember to manually select iso file path for main and guest additions

If cannot sudo apt update after fresh installation,
https://unix.stackexchange.com/questions/179954/username-is-not-in-the-sudoers-file-this-incident-will-be-reported

Then update everything by,
```
sudo apt update
sudo apt upgrade
```
If SnapStore needs upgrading,
```
$ sudo killall snap-store
$ sudo snap refresh snap-store
```
Best to save a snapshot now...

Install VS Code on SnapStore

Install Anaconda like https://linuxhint.com/update-all-packages-ubuntu/

Restart to see Anaconda on VS Code


