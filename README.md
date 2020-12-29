# RPi4 overclock 2.0GHz

 
 ## Step 1
```sh
$ sudo apt update
$ sudo apt dist-upgrade
```

### Reboot
```sh
$ reboot
```

 ## Step 2 Checking the default speed of CPU
```sh
$ cat /sys/devices/system/cpu/cpu0/cpufreq/scaling_cur_freq
```

 ## Step 3 Let’s start overclocking!
```sh
$ sudo nano /boot/config.txt
```
* Change the config settings to
```sh
over_voltage=6
arm_freq=2000
gpu_freq=750
```
### Reboot your Raspberry Pi 4 now and run:
```sh
$ watch -n 1 vcgencmd measure_clock arm
```
