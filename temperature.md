# Temperature test

vcgencmd measure_temp

# Disck speed test

lsblk
sudo hdparm -t /dev/mmcblk0

# Throtling test

vcgencmd get_throttled