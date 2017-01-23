#Raspberry Setup

## Enable SSH

```
$ sudo raspi-config
```
Advanced Options -> SSH -> Enable Yes


## Enable Wifi - command line

```
$ sudo iwlist wlan0 scan| grep "ESSID"
```
choose the wifi you would like to connect to

```
$ sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
```

Add the below text after the last line of the file, save file

```
network={
    ssid="XXXXXX"
    psk="Password of the wifi network"
}
```

Reboot 
```
$ sudo reboot
```

## Enable us keyboard

```
$ sudo nano /etc/default/keyboard
```

Change value to XKBLAYOUT="us", save file

Reboot
```
$ sudo reboot
```

## Enable static IP

```
$ sudo nano /etc/network/interfaces
```
Add below with values 
network
netmask
gateway
