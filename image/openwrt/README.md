# Flash via telnet
windows side:  
busybox nc -l -p <port> < openwrt.bin
                                     
router side:                                       
cd /tmp              
nc <IPv4 address> <port> > openwrt.bin  
mtd_write -e Kernel -r write openwrt.bin Kernel  
