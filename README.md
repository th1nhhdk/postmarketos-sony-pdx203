## status
boots, without working screen
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
