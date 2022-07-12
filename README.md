# vnc-server-setup

## Prepare server

sudo apt-get update

sudo apt-get install lightdm

**sudo reboot**

sudo apt-get install x11vnc

## Set password and create service

x11vnc -storepasswd -- set password for vnc 

sudo cp ~/.vnc/passwd /etc/vnc.passwd

sudo nano /lib/systemd/system/x11vnc.service -- copy content of x11vnc.service from this repo

## Run vnc service

systemctl daemon-reload

systemctl enable x11vnc.service

systemctl start x11vnc.service

systemctl status x11vnc.service

## Additional

disable screenlock
