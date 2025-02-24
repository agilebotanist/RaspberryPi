# ROM update

```
sudo rpi-eeprom-update 
```

# More info
Type the following command in the terminal:
„sudo rpi-eeprom-config --edit“ – Hit „enter“ (Note the double - - !!!)
a small window like below in the image should open.
Use the arrows on the keyboard to move the cursor (here green block) to the end of the listing.
Type the following line:
„PSU_MAX_CURRENT=5000“

http://blog.dddac.com/wp-content/uploads/Flash-RPi5-and-adding-5000mA-Line-tutorial.pdf


# Addition (2025-01-15)

If you are using an M4 iPad Pro, this step may be necessary:

```
rpi-eeprom-config -e
```

Add the following text at the bottom of the file, save, exit, reboot:

```
PSU_MAX_CURRENT=3000
```
