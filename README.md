# mipad2_linux_bluetooth_firmware

*thanks iiowoii3389 first!*

here is bcm4356a2 nvram and hcd files backup (extract from iiowoii3389 bliss os 11) , work with iiowoii3389 's kernel work "https://github.com/linux-latte/linux-latte"

my problem is bt can't find device when follow his step install kernel deb and cp brcmfmac4356-pcie.txt on mipad2 debian12 
dmesg just said cant find BCM4356A2.hcd 

do search then get blissos 11 and blissos 15 from iiowoii3389 ,and bt only work in bos 11 
so get hcd and brcmfmac4356-pcie.txt by extract bos 11 system.img and put in debian12
but still got dmesg "kernel: Bluetooth: hci0: Frame reassembly failed (-84)"
again some google stuff , i finally guess this error may cause by kernel 6.1 bt change, 
try iiowoii3389 's kernel 5.15.80 and all done ...

# usage

1. follow iiowoii3389 step install os
2. install kernel 5.15.80 deb , *NOT* use kernel 6.1.20
3. put here txt and hcd in /lib/firmware/brcm, *NOT* use iiowoii3389 repository 's brcmfmac4356-pcie.txt
