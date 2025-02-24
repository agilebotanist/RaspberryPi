# Tiger VNC setup

>Note: USB auto-mount fail when tiger is running

## Install

```
sudo apt install tigervnc-standalone-server
```

## Config

```
session = some_win

geometry = 1194x834

```

## Enable

```
sudo systemctl status tigervncserver@\:1.service 
```

## More instractions


The steps below are under the assumption that you have installed TigerVNC and done nothing more.

Firstly I signed into the user account and created a vnc password by executing the command:

```
$ vncpasswd
```

I did not set a view only password when prompted.

Next I modified the vncserver.user file located in: /etc/tigervnc/ and added my user by following the examples in the file.

After saving my changes I copied the user environment config template from the /etc/tigervnc/ directory to my user account home directory by executing the following command:

$ cp /etc/tigervnc/vncserver-config-mandatory ~/.vnc/config
After copying the template, I edited the config file to define my session and desired screen resolution:

```
session=xfce4-session
geometry=1920x1080

```
Next I copied the systemd service template by executing the command:

```
$ sudo cp /lib/systemd/system/vncserver@.service /etc/systemd/system/vncserver@:1.service
```
