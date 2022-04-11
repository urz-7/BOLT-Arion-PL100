# Flash via telnet
windows cmd:  
> busybox nc -l -p \<port> < openwrt.bin  
                                     
router side:                                       
> cd /tmp              
> nc \<IPv4 address> \<port> > openwrt.bin  
> mtd_write -e Kernel -r write openwrt.bin Kernel  

busybox for windows:  
> https://frippery.org/files/busybox/busybox.exe  
> https://frippery.org/files/busybox/busybox64.exe
