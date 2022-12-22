
ACCELEROMETER_QUERY

TEST_RESONANCES AXIS=X
TEST_RESONANCES AXIS=Y


/tmp/resonances_y_20221118_135331.csv
/tmp/resonances_x_20221118_133443.csv
(no permission to delete these and no sudo, will have to clean up later)

ssh creality@sonicpad
pass:creality

creality@spad-7580:~$ pwd
/usr/share/klipper

~/scripts/calibrate_shaper.py /tmp/resonances_x_20221118_133443.csv -o /tmp/shaper_calibrate_x.png
~/scripts/calibrate_shaper.py /tmp/resonances_y_20221118_135331.csv -o /tmp/shaper_calibrate_y.png


-ash: /usr/share/klipper/scripts/calibrate_shaper.py: not found
creality@spad-7580:/usr$ ~/scripts/calibrate_shaper.py /tmp/resonances_x_20221118_133443.csv -o /tmp/shaper_calibrate_x.
png

Fitted shaper 'zv' frequency = 101.0 Hz (vibrations = 30.5%, smoothing ~= 0.021)
To avoid too much smoothing with 'zv', suggested max_accel <= 39800 mm/sec^2
Fitted shaper 'mzv' frequency = 59.4 Hz (vibrations = 4.3%, smoothing ~= 0.058)
To avoid too much smoothing with 'mzv', suggested max_accel <= 10400 mm/sec^2
Fitted shaper 'ei' frequency = 82.6 Hz (vibrations = 9.2%, smoothing ~= 0.047)
To avoid too much smoothing with 'ei', suggested max_accel <= 12700 mm/sec^2
Fitted shaper '2hump_ei' frequency = 75.6 Hz (vibrations = 0.0%, smoothing ~= 0.094)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 6400 mm/sec^2
Fitted shaper '3hump_ei' frequency = 90.4 Hz (vibrations = 0.0%, smoothing ~= 0.100)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 6000 mm/sec^2
Recommended shaper is 2hump_ei @ 75.6 Hz



creality@spad-7580:/usr$ ~/scripts/calibrate_shaper.py /tmp/resonances_y_20221118_135331.csv -o /tmp/shaper_calibrate_y.png
Fitted shaper 'zv' frequency = 55.2 Hz (vibrations = 16.3%, smoothing ~= 0.057)
To avoid too much smoothing with 'zv', suggested max_accel <= 11900 mm/sec^2
Fitted shaper 'mzv' frequency = 37.2 Hz (vibrations = 1.1%, smoothing ~= 0.147)
To avoid too much smoothing with 'mzv', suggested max_accel <= 4100 mm/sec^2
Fitted shaper 'ei' frequency = 48.0 Hz (vibrations = 0.0%, smoothing ~= 0.140)
To avoid too much smoothing with 'ei', suggested max_accel <= 4300 mm/sec^2
Fitted shaper '2hump_ei' frequency = 60.6 Hz (vibrations = 0.0%, smoothing ~= 0.147)
To avoid too much smoothing with '2hump_ei', suggested max_accel <= 4100 mm/sec^2
Fitted shaper '3hump_ei' frequency = 73.8 Hz (vibrations = 0.0%, smoothing ~= 0.150)
To avoid too much smoothing with '3hump_ei', suggested max_accel <= 4000 mm/sec^2
Recommended shaper is ei @ 48.0 Hz



ls -la /mnt/UDISK/.crealityprint/upload
ls -la /mnt/UDISK/.crealityprint/videos
ls -la /mnt/UDISK/printer_config
ls -la /mnt/UDISK/printer_logs

cp /tmp/*.png /mnt/UDISK/printer_config



creality@spad-7580:~$ id
uid=500(creality) gid=500(creality) groups=500(creality)

#info
creality@spad-7580:~$ uname -a
Linux spad-7580 4.9.191 #56 SMP PREEMPT Mon Oct 31 07:17:35 UTC 2022 aarch64 GNU/Linux

creality@spad-7580:~$ cat /proc/version
Linux version 4.9.191 (wuhui@ubuntu1804) (gcc version 6.4.1 (OpenWrt/Linaro GCC 6.4-2017.11 2017-11) ) #56 SMP PREEMPT Mon Oct 31 07:17:35 UTC 2022

/etc/passwd
root:x:0:0:root:/root:/bin/ash
daemon:*:1:1:daemon:/var:/bin/false
ftp:*:55:55:ftp:/home/ftp:/bin/false
network:*:101:101:network:/var:/bin/false
nobody:*:65534:65534:nobody:/var:/bin/false
creality:x:500:500::/usr/share/klipper:/bin/ash
ntp:x:123:123:ntp:/var/run/ntp:/bin/false

/etc/group
root:x:0:
daemon:x:1:
adm:x:4:
mail:x:8:
audio:x:29:
www-data:x:33:
ftp:x:55:
users:x:100:
network:x:101:
creality:x:500:
nogroup:x:65534:
ntp:x:123:ntp

creality@spad-7580:~$ ls -l /etc/init.d/*
-rwxr-xr-x    1 root     root           234 Aug 26 03:18 /etc/init.d/S99swupdate_autorun
-rwxr-xr-x    1 root     root          1703 Aug  1 02:32 /etc/init.d/adbd
-rwxrwxr-x    1 root     root          1013 Oct 28 05:31 /etc/init.d/audio_setting
-rwxr-xr-x    1 root     root           281 Aug  1 02:32 /etc/init.d/avahi-daemon
-rwxrwxr-x    1 root     root          4473 Oct 28 05:31 /etc/init.d/boot
-rwxrwxr-x    1 root     root           874 Oct 28 05:31 /etc/init.d/browser
-rwxr-xr-x    1 root     root           745 Oct 28 05:31 /etc/init.d/cron
-rwxr-xr-x    1 root     root          1064 Oct 28 05:31 /etc/init.d/cxgunicorn
-rwxr-xr-x    1 root     root           588 Oct 28 05:31 /etc/init.d/cxwatchdog
-rwxr-xr-x    1 root     root           376 Aug  1 02:32 /etc/init.d/dbus
-rwxrwxr-x    1 root     root           946 Oct 28 05:31 /etc/init.d/done
-rwxr-xr-x    1 root     root          4122 Aug  1 02:32 /etc/init.d/dropbear
-rwxr-xr-x    1 root     root           302 Aug  1 02:32 /etc/init.d/fontconfig
-rwxr-xr-x    1 root     root           430 Oct 27 15:57 /etc/init.d/fstab
-rwxr-xr-x    1 root     root          1134 Oct 28 05:31 /etc/init.d/klipper_mcu
-rwxr-xr-x    1 root     root          1194 Oct 28 05:31 /etc/init.d/klipper_service
-rwxr-xr-x    1 root     root          2347 Aug  1 02:32 /etc/init.d/log
-rwxr-xr-x    1 root     root           310 Oct 28 05:31 /etc/init.d/monitor_service
-rwxr-xr-x    1 root     root          1068 Oct 28 05:31 /etc/init.d/moonraker_service
-rwxrwxr-x    1 root     root          2763 Aug  1 02:32 /etc/init.d/network
-rwxr-xr-x    1 root     root           426 Oct 27 15:57 /etc/init.d/nginx
-rwxr-xr-x    1 root     root          1932 Aug  1 02:32 /etc/init.d/ntpd
-rwxr-xr-x    1 root     root           157 Sep 23 09:29 /etc/init.d/play
-rwxr-xr-x    1 root     root           227 Oct 27 15:57 /etc/init.d/restore_service
-rwxrwxr-x    1 root     root           277 Oct 28 05:31 /etc/init.d/sys_led
-rwxrwxr-x    1 root     root           186 Oct 28 05:31 /etc/init.d/sysctl
-rwxrwxr-x    1 root     root           533 Oct 28 05:31 /etc/init.d/sysfixtime
-rwxrwxr-x    1 root     root          1658 Oct 28 05:31 /etc/init.d/system
-rwxrwxr-x    1 root     root          1389 Aug 26 03:18 /etc/init.d/udev
-rwxrwxr-x    1 root     root           106 Oct 28 05:31 /etc/init.d/umount
-rwxrwxr-x    1 root     root           122 Oct 28 05:31 /etc/init.d/usbc0
-rwxr-xr-x    1 root     root           570 Aug  1 02:32 /etc/init.d/webcam_service
-rwxrwxr-x    1 root     root          5511 Oct 28 05:31 /etc/init.d/wifi
-rwxr-xr-x    1 root     root           374 Aug 26 03:18 /etc/init.d/wifi_daemon
-rwxr-xr-x    1 root     root          1209 Aug 26 03:18 /etc/init.d/wpa_supplicant

creality@spad-7580:~$ echo $PATH
/usr/sbin:/usr/bin:/sbin:/bin






get root
edit machine.py #115
add set shadow hash

get console access

/usr/share/klippy-env/bin/python ./klippy/console.py /tmp/pseudoserial

  config_digital_out oid=%c pin=%u value=%c default_value=%c max_duration=%u
set_digital_out pin=PA0 value=1
set_digital_out pin=PA1 value=1


; free /dev/serial/by-id/usb_serial_2 if klipper has lock
/usr/share/klippy-env/bin/python /usr/share/klipper/klippy/console.py /dev/serial/by-id/usb_serial_2
clear_shutdown
set_digital_out pin=PA3 value=1
set_digital_out pin=PA3 value=0
