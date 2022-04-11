# Flash Openwrt.bin via telnet  
Enable telnet on router:  

Method 1  
-Backup config  
-Upload mod telnet config  

Method 2  
-Connect USB to TTL. baudrate 57600  
-type:  
> busybox telnetd -l /bin/sh  


Open putty. telnet 192.168.1.1  
Rename firmware file to openwrt.bin  

windows cmd:  
> busybox nc -l -p \<port> < openwrt.bin  
                                     
router side:                                       
> cd /tmp              
> nc \<IPv4 address> \<port> > openwrt.bin  
> mtd_write -e Kernel -r write openwrt.bin Kernel  

busybox for windows:  
> https://frippery.org/files/busybox/busybox.exe  
> https://frippery.org/files/busybox/busybox64.exe

# Install Breed Bootloader:
Make sure have internet  
Open putty  
ssh 192.168.1.1 port 22  
> opkg update && opkg install kmod-mtd-rw  
> insmod mtd-rw i_want_a_brick=1  
> wget https://breed.hackpascal.net/breed-mt7621-gehua-ghl-r-001.bin -O /tmp/breed-mt7621-gehua-ghl-r-001.bin  
> mtd -e u-boot -r write /tmp/breed-mt7621-gehua-ghl-r-001.bin u-boot  

How to access breed (English language):  
Hold WPS button + Power ON around 10 seconds  
Open Chrome Browser 192.168.1.1  
right click mouse > Translate to English

