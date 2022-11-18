
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


-ash: /usr/share/klipper/klipper/scripts/calibrate_shaper.py: not found
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