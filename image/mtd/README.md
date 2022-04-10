# cat /proc/mtd

dev:    size   erasesize  name

mtd0: 02000000 00010000 "ALL"

mtd1: 00020000 00010000 "Bootloader"

mtd2: 00020000 00010000 "Config"

mtd3: 00010000 00010000 "Factory"

mtd4: 00fb0000 00010000 "Kernel"

for dump:

dd if=/dev/mtdblock0 of=/tmp/mtd0.bin

dd if=/dev/mtdblock1 of=/tmp/mtd1.bin

dd if=/dev/mtdblock2 of=/tmp/mtd2.bin

dd if=/dev/mtdblock3 of=/tmp/mtd3.bin

dd if=/dev/mtdblock4 of=/tmp/mtd4.bin

or

cat /dev/mtdblock0 > /tmp/mtd0.bin

cat /dev/mtdblock1 > /tmp/mtd1.bin

cat /dev/mtdblock2 > /tmp/mtd2.bin

cat /dev/mtdblock3 > /tmp/mtd3.bin

cat /dev/mtdblock4 > /tmp/mtd4.bin
