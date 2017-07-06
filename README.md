# ubuntu_wireless_driver_fix
first repo

+FOR WIRELESS DRIVER IN UBUNTU 14.04 (Broadcom Corporation)-

Make sure you have a working wired connection to the internet 


$ lspci -knn | grep Net -A2

if given below is the o/p, please continue

{ 01:00.0 Network controller [0280]: Broadcom Corporation BCM43142 802.11b/g/n [14e4:4365] (rev 01)
    Subsystem: Dell Device [1028:0018]
    Kernel driver in use: bcma-pci-bridge
}
$ sudo apt-get --purge remove bcmwl-kernel-source

$ sudo apt-get install bcmwl-kernel-source

while installing, permission to insecure boot is asked and click ok. then give a 16 bit password. after installation, reboot.

while restarting, click on change boot-->insecure boot-->type asked chars of password

then take ubuntu 14.04, and wifi is installed. 


