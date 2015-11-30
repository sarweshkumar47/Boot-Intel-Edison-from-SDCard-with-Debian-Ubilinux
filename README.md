# Boot-Intel-Edison-from-SDCard-with-Debian-Ubilinux
##Boot Intel Edison board with the Root Filesystem on an external storage


Before following any of these steps, make sure you have booted ubilinux or debian os 
(from Emutexlabs) on Intel Edison.


###Prepare External Storage (MicroSD Card)
1. You need to have a SD card formatted with ext4 file system to store the root file system
2. Download and unpack Debian image from emutexlabs website
3. In the unpacked directory (with the "flashall.sh" script) run the following commands to
   prepare the SD card. These commands mount the edison-image-edison.ext4 rootfs image and 
   copy the contents onto the SD card
  
        sudo su
        mkdir Rootfs
        mount ./edison-image-edison.ext4 Rootfs
        cp -a Rootfs/* media/saru/eb361b92-c285-44a6-9f32-da393c879487
        sync
4. Eject the SD Card and now it is ready to boot

      ![image](https://github.com/sarweshkumar47/Boot-Intel-Edison-from-SDCard-with-Debian-Ubilinux/blob/master/Screenshots/s1.png?raw=true)
