## status
boots, without working screen

also for some reason pmOS cannot find my root or boot partition

(output from `wait_root_partition`)
```
Could not find the rootfs.
Maybe you need to insert the sdcard, if your device has
any? Trying again in one second...
ERROR!!!: Invalid screen size: 0x0
1644x3840 @ 139x325mm, dpi=300, logo_size_px=495.000000
SPACE! Linux 
SPACE! Linux 6.4.0-rc2 
SPACE! Linux 6.4.0-rc2 | 
SPACE! ERROR: 
SPACE! ERROR: root 
SPACE! ERROR: root partition 
SPACE! ERROR: root partition not 
LINE SPLIT, 31 ERROR: root partition not found
```

![Screenshot from 2023-06-02 14-29-27](https://github.com/th1nhhdk/postmarketos-sony-pdx203/assets/58503327/01a817a1-0656-4fd1-98d4-fb87b85cf474)

### install
```
mv -v ./*-sony-pdx203 ~/.local/var/pmbootstrap/cache_git/pmaports/device/testing/
pmbootstrap build --force device-sony-pdx203

# pmbootstrap init here

pmbootstrap install --sdcard=<path>

# adb reboot bootloader
fastboot flash dtbo ./emptystuff.img
pmbootstrap flasher flash-kernel
```
