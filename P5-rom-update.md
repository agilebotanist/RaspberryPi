# ROM update

```
sudo rpi-eeprom-update 
```



# Addition (2025-01-15)

If you are using an M4 iPad Pro, this step may be necessary:

```
rpi-eeprom-config -e
```

Add the following text at the bottom of the file, save, exit, reboot:

```
PSU_MAX_CURRENT=3000
```
